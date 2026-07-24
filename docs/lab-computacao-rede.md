# Projeto: Configuração e Gerenciamento de Máquinas Virtuais no Azure  

## 1. Criação da Máquina Virtual  
No portal do Azure, ao escolher a opção **Máquina Virtual do Azure**, você pode criar uma nova máquina virtual hospedada pelo Azure. A configuração pode ser feita de forma **personalizada** ou utilizando uma **configuração pré-definida**.  

- **Configuração Personalizada:** Permite ajustar todos os parâmetros da VM, como sistema operacional, recursos de CPU, memória e armazenamento.  
- **Configuração Pré-definida:** Oferece uma configuração rápida com padrões para facilitar a criação.  

---

## 2. Configuração de Escala e Conjunto de Dimensionamento (VM Scale Set)  
A escala permite que você dimensione suas máquinas virtuais de acordo com a demanda.  

- **Escalabilidade Automática:** O Azure ajusta a quantidade de VMs ativas conforme a demanda de tráfego.  
- **Alta Disponibilidade:** O tráfego e a carga de trabalho são distribuídos entre as VMs de forma otimizada.  

---

## 3. Seleção do Tamanho da VM  
O tamanho da VM deve ser escolhido com base nas necessidades de recursos:  

- **Básicas:** Para testes ou ambientes com baixo consumo.  
- **Alto Desempenho:** Para workloads exigentes (banco de dados, análises intensivas etc.).  

---

## 4. Porta RDP 3389 Aberta  
Para acesso remoto via **Remote Desktop Protocol (RDP)**:  

- Mantenha a porta **3389** aberta.  
- Configure regras de segurança para restringir o acesso apenas a **IPs confiáveis**.  
- Utilize **firewalls** para maior proteção.  

---

## 5. Exclusão de Disco e IP Público/NIC ao Excluir a VM  
Ao excluir uma VM, é possível configurar a remoção automática de recursos associados:  

- **Disco de Dados**  
- **IP Público**  
- **NIC (Network Interface Card)**  

Isso evita custos extras com recursos não utilizados caso a máquina seja excluida.  

---

## 6. Desligamento Automático e Notificação  
O Azure permite desligamento automático em horários agendados.  

- **Agendamento:** Configure horários via **Azure Automation** ou **Logic Apps**.  
- **Economia de Custos:** Evita consumo fora do horário necessário.  
- **Notificação:** Administradores podem receber alertas (e-mail, SMS etc.) antes do desligamento, prevenindo perda de dados.  
- **Importante:** O Azure **não inicia a VM automaticamente**. O agendamento de inicialização deve ser configurado separadamente.  

---

## 7. Área de Trabalho Virtual do Azure  
Permite oferecer uma experiência de desktop remoto para usuários finais.  

- **Gerenciamento Centralizado:** Controle de desktops e aplicativos em um único ponto.  
- **Segurança e Acessibilidade:** Acesso remoto seguro de qualquer lugar.  

---

## 8. Host Pessoal ou Pool  
- **Host Pessoal:** Cada usuário recebe uma VM dedicada.  
- **Pool de Hosts:** Vários usuários acessam VMs dentro de um pool, otimizando recursos.  

---

## 9. Balanceamento de Carga  
O **Azure Load Balancer** distribui automaticamente o tráfego entre várias VMs.  

- **Alta Disponibilidade:** Redireciona o tráfego em caso de falha.  
- **Otimização de Performance:** Mantém a estabilidade dos serviços.  

---

## 10. Limite Máximo de Sessões  
No **Azure Virtual Desktop**, é possível definir o número máximo de sessões simultâneas.  

- **Controle de Sobrecarga:** Evita sobrecarga das VMs.  
- **Escalabilidade:** Permite adicionar novas VMs quando o limite é alcançado.  

---

## 📌 Conclusão  
Este projeto aborda as principais práticas de configuração e gerenciamento de VMs no Azure:  

- Criação de VMs (personalizadas ou pré-definidas).  
- Escalabilidade com **VM Scale Sets** e **Azure Load Balancer**.  
- Acesso remoto via **Azure Virtual Desktop**.  
- Gerenciamento de sessões, desligamento agendado e notificações.  

Com essas práticas, é possível garantir uma infraestrutura **eficiente, escalável e segura**, aproveitando o potencial do Azure para reduzir custos e melhorar a experiência dos usuários.  
