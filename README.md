# Windows Support Lab

**Documentação para problemas comuns de Windows: impressoras, conectividade, desempenho, escalonamento, segurança e checklist de atendimento.**

---

## 📋 Visão Geral / Overview

Repositório de documentação técnica para resolução de problemas comuns no Windows, cobrindo impressoras, conectividade, desempenho, escalonamento, segurança e checklist de atendimento.

Technical documentation repository for common Windows troubleshooting, covering printers, connectivity, performance, escalation, security, and service checklists.

---

## ⚠️ Aviso / Disclaimer

> **Projeto Pessoal / Laboratório / Personal Project / Laboratory Project**
>
> Este projeto é destinado apenas para fins educacionais e de laboratório. **Não inclui comandos destrutivos.**
>
> This project is for educational and laboratory purposes only. **No destructive commands are included.**

---

## 📁 Estrutura do Projeto / Project Structure

```
windows-support-lab/
├── README.md
├── problemas/
│   ├── impressoras.md
│   ├── conectividade.md
│   ├── desempenho.md
│   └── atualizacoes.md
├── escalonamento.md
├── seguranca.md
└── checklist_atendimento.md
```

---

## 🖨️ Problemas Comuns / Common Issues

### Impressoras / Printers

**Problema:** Impressora não imprime
1. Verificar se está online e sem erros
2. Verificar conexão USB/rede
3. Reiniciar o serviço "Spooler de Impressão"
4. Verificar se há documentos pendentes na fila
5. Reinstalar drivers se necessário

**Problema:** Impressão borrada / manchar
1. Verificar nível de toner/tinta
2. Executar limpeza de bicos (impressoras jato de tinta)
3. Verificar qualidade do papel
4. Executar alinhamento de cabeçote

**Problema:** Impressora não encontrada na rede
1. Verificar se impressora e PC estão na mesma rede
2. Verificar configuração de IP da impressora
3. Reiniciar impressora e roteador
4. Adicionar impressora novamente via Painel de Controle

### Conectividade / Connectivity

**Problema:** Sem acesso à internet
1. Verificar se Wi-Fi/cabo está conectado
2. Executar `ipconfig /all` e verificar IP
3. Executar `ping 8.8.8.8`
4. Executar `ipconfig /flushdns`
5. Verificar configurações de proxy

**Problema:** Wi-Fi conecta mas não navega
1. Esquecer a rede e reconectar
2. Executar `netsh winsock reset`
3. Reiniciar adaptador de rede
4. Verificar configuração DHCP

**Problema:** Rede doméstica não acessa recursos compartilhados
1. Verificar se rede está em perfil "Privada"
2. Verificar compartilhamento de rede
3. Verificar grupo de trabalho

### Desempenho / Performance

**Problema:** Computador lento
1. Verificar uso de CPU, memória e disco no Gerenciador de Tarefas
2. Verificar programas de inicialização
3. Verificar espaço em disco
4. Executar `sfc /scannow` para verificar arquivos do sistema
5. Verificar atualizações pendentes

**Problema:** Boot lento
1. Desabilitar programas desnecessários na inicialização
2. Verificar integridade do disco
3. Verificar tempo de resposta do disco

### Atualizações / Updates

**Problema:** Atualização do Windows não instala
1. Executar o Solucionador de Problemas de Atualização
2. Limpar pasta `SoftwareDistribution`
3. Executar `sfc /scannow` e `DISM`
4. Reiniciar e tentar novamente

---

## 📈 Escalonamento / Escalation

### Quando Escalonar

1. **Nível 1 → Nível 2:**
   - Problema não resolvido após 30 minutos
   - Problema envolve configuração de rede complexa
   - Problema requer acesso administrativo não disponível
   - Problema de software específico ou corrupção de sistema

2. **Nível 2 → Nível 3:**
   - Problema requer análise profunda de logs
   - Problema de hardware necessitando substituição
   - Problema de segurança (violação, malware)
   - Problema de infraestrutura (servidores, AD)

### Informações a Fornecer

- Descrição detalhada do problema
- Passos já realizados
- Logs e capturas de tela
- Informações do sistema (SO, versão)
- Impacto no negócio

---

## 🔒 Segurança / Security

### Boas Práticas

1. Sempre verificar a origem de arquivos/e-mails
2. Manter sistema operacional atualizado
3. Usar senhas fortes e únicas
4. Não compartilhar credenciais
5. Usar autenticação multifator quando disponível
6. Bloquear computador ao sair (`Win + L`)

### Problemas Comuns de Segurança

**Problema:** Mensagem de malware/vírus detectado
1. Desconectar da rede para evitar propagação
2. Executar análise completa com antivirus
3. Verificar programas instalados recentemente
4. Se persistir, escalar para equipe de segurança

**Problema:** Acesso não autorizado
1. Alterar senha imediatamente
2. Verificar atividade suspeita
3. Desabilitar conta comprometida se necessário
4. Escalonar para equipe de segurança

**Problema:** Conta travada
1. Verificar tentativas de login falhas
2. Desbloquear conta via AD ou localmente
3. Investigar causa raiz
4. Educar usuário sobre boas práticas

---

## ✅ Checklist de Atendimento / Service Checklist

### Recebimento
- [ ] Registrar chamado com descrição clara
- [ ] Coletar informações do usuário (nome, setor, telefone)
- [ ] Classificar prioridade (Baixa/Média/Alta/Crítica)
- [ ] Categorizar problema (Hardware/Software/Rede/Outro)

### Triagem
- [ ] Reproduzir o problema se possível
- [ ] Identificar escopo (um usuário ou múltiplos)
- [ ] Verificar se há solução conhecida (KB)
- [ ] Definir SLA esperado

### Diagnóstico
- [ ] Coletar informações do sistema
- [ ] Verificar logs relevantes
- [ ] Testar hipóteses
- [ ] Documentar descobertas

### Resolução
- [ ] Aplicar solução
- [ ] Testar para confirmar resolução
- [ ] Documentar solução aplicada
- [ ] Informar usuário

### Encerramento
- [ ] Confirmar com usuário que está tudo funcionando
- [ ] Coletar feedback/satisfação
- [ ] Fechar chamado com observações
- [ ] Arquivar documentação se aplicável

---

## 📝 Licença / License

Projeto pessoal / laboratório. Uso educacional.
