---
description: Os códigos de motivo de desligamento são usados pelas funções ExitWindowsEx e InitiateSystemShutdownEx no parâmetro dwReason. Um número máximo de \_ razões máximas \_ que os códigos de motivo serão processados pelo sistema. O \_ número máximo \_ de razões é definido em Reason. h.
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: Códigos de motivo de desligamento do sistema (motivo. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef40cf53afd3abaf261e15f2caba735dea7963ee5b5f19cebc78c63a373962fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073196"
---
# <a name="system-shutdown-reason-codes"></a>Códigos de motivo de desligamento do sistema

Os códigos de motivo de desligamento são usados pelas funções [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) no parâmetro *dwReason* .

Um número máximo de \_ razões máximas \_ que os códigos de motivo serão processados pelo sistema. O \_ número máximo \_ de razões é definido em Reason. h.

A seguir estão os sinalizadores de motivo principal. Eles indicam o tipo de problema geral.



| Constante/valor                                                                                                                                                                                                                                                                                 | Descrição                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal do \_ aplicativo**</dt> <dt>0x00040000</dt> </dl>             | Problema do aplicativo.<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**SHTDN \_ MOTIVO do 0x00010000 de \_ \_ hardware principal**</dt> <dt></dt> </dl>                      | Problema de hardware.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**SHTDN \_ MOTIVO \_ da \_ \_ API herdada principal**</dt> <dt>0x00070000</dt> </dl>               | A função [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) foi usada em vez de [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa).<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_**</dt> do <dt>0x00020000</dt> de sistema operacional principal </dl> | Problema do sistema operacional.<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal- \_ outro**</dt> <dt>0x00000000</dt> </dl>                               | Outro problema.<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**SHTDN \_ MOTIVO do 0x00060000 de \_ \_ energia principal**</dt> <dt></dt> </dl>                               | Falha de energia.<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**SHTDN \_ MOTIVO do 0x00030000 de \_ \_ software principal**</dt> <dt></dt> </dl>                      | Problema de software.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal do \_ sistema**</dt> <dt>0x00050000</dt> </dl>                            | Falha do sistema.<br/>                                                                                                                                         |



A seguir estão os sinalizadores de motivo secundários. Eles modificam o sinalizador de motivo principal especificado. Você pode usar qualquer motivo secundário em conjunto com qualquer motivo principal, mas algumas combinações não fazem sentido.



| Constante/valor                                                                                                                                                                                                                                                                                                    | Descrição                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ BLUESCREEN**</dt> <dt>0x0000000F</dt> de menor </dl>                                   | Evento de falha de tela azul.<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ CORDUNPLUGGED**</dt> <dt>0x0000000b</dt> de menor </dl>                          | Desconectado.<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**SHTDN \_ MOTIVO 0x00000007 de \_ \_ disco secundário**</dt> <dt></dt> </dl>                                                     | Disk.<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x0000000c de \_ \_ ambiente secundário**</dt> <dt></dt> </dl>                                | Ambiente.<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ \_ Driver de hardware menor**</dt> <dt>0x0000000d</dt> </dl>                   | Driver.<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x00000011 de \_ \_ hotfix secundário**</dt> <dt></dt> </dl>                                               | Hot Fix.<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ da \_ \_ desinstalação do hotfix secundário**</dt> <dt>0x00000017</dt> </dl>                | Desinstalação de correção automática.<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x00000005 de \_ menor \_ paralisação**</dt> <dt></dt> </dl>                                                     | Sem resposta.<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**SHTDN \_ MOTIVO \_ da \_ instalação secundária**</dt> <dt>0x00000002</dt> </dl>                             | Instalação.<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ manutenção secundária**</dt> <dt>0x00000001</dt> </dl>                                | Manter.<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**SHTDN \_ MOTIVO 0x00000019 do \_ \_ MMC secundário**</dt> <dt></dt> </dl>                                                        | Problema do MMC.<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ \_ conectividade de rede pequena**</dt> <dt>0x00000014</dt> </dl>    | Conectividade de rede.<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ NETWORKCARD**</dt> <dt>0x00000009</dt> de menor </dl>                                | Placa de rede.<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secundário- \_ outros**</dt> <dt>0x00000000</dt> </dl>                                                  | Outro problema.<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ OTHERDRIVER**</dt> <dt>0x0000000e</dt> de menor </dl>                                | Outro evento de driver.<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**SHTDN \_ MOTIVO \_ da \_ \_ fonte de energia secundária**</dt> <dt>0x0000000A</dt> </dl>                            | Fonte de energia.<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x00000008 de \_ \_ processador secundário**</dt> <dt></dt> </dl>                                      | Processador.<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**SHTDN \_ MOTIVO \_ da \_ reconfiguração mínima**</dt> <dt>0x00000004</dt> </dl>                                         | Reconfigurar.<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ segurança mínima**</dt> <dt>0x00000013</dt> </dl>                                         | Problema de segurança.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_ SECURITYFIX**</dt> <dt>0x00000012</dt> de menor </dl>                                | Patch de segurança.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secundário \_ de \_ desinstalação do SECURITYFIX**</dt> <dt>0x00000018</dt> </dl> | Desinstalação do patch de segurança.<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secundário do \_ Service Pack**</dt> <dt>0x00000010</dt> </dl>                                | Service Pack.<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ \_ desinstalação secundária do Service Pack**</dt> <dt>0x00000016</dt> </dl> | Desinstalação do Service Pack.<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**SHTDN \_ MOTIVO \_ secundário de \_ termsrv**</dt> <dt>0x00000020</dt> </dl>                                            | Serviços de terminal.<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x00000006 de \_ \_ instabilidade secundário**</dt> <dt></dt> </dl>                                         | Ocorrer.<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**SHTDN \_ MOTIVO \_ da \_ atualização secundária**</dt> <dt>0x00000003</dt> </dl>                                            | Atualização.<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**SHTDN \_ MOTIVO 0x00000015 de \_ \_ WMI secundário**</dt> <dt></dt> </dl>                                                        | Problema de WMI.<br/>                     |



Os sinalizadores opcionais a seguir fornecem informações adicionais sobre o evento.



| Constante/valor                                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**SHTDN \_ MOTIVO do sinalizador de 0x40000000 \_ \_ \_ definido pelo usuário**</dt> <dt></dt> </dl> | O código do motivo é definido pelo usuário. Para obter mais informações, consulte Definindo um código de motivo personalizado. <br/> Se esse sinalizador não estiver presente, o código do motivo será definido pelo sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**SHTDN \_ MOTIVO \_ do \_ sinalizador demarcado**</dt> <dt>0x80000000</dt> </dl>                 | O desligamento foi planejado. O sistema gera um arquivo de dados de estado do sistema (SSD). Esse arquivo contém informações de estado do sistema, como processos, threads, uso de memória e configuração. <br/> Se esse sinalizador não estiver presente, o desligamento não foi planejado. As opções de notificação e relatório são controladas por um conjunto de políticas. Por exemplo, depois de fazer logon, o sistema exibirá uma caixa de diálogo informando o desligamento não planejado se a política tiver sido habilitada. Um arquivo SSD será criado somente se a política SSD estiver habilitada no sistema. O administrador pode usar [Relatório de Erros do Windows](../wer/windows-error-reporting.md) para enviar os dados do SSD para um local central ou para a Microsoft.<br/> |



## <a name="remarks"></a>Comentários

As combinações a seguir são reconhecidas pelo sistema. A tabela indica a cadeia de caracteres exibida no Rastreador de Eventos de Desligamento e fornece uma descrição mais detalhada. A cadeia de caracteres padrão é "Nenhum título por esse motivo pôde ser encontrado".



| Combinação                                                                                                | Descrição                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ HUNG                                            | "Aplicativo: sem resposta" Uma reinicialização ou desligamento não planejado para solucionar problemas de um aplicativo sem resposta.<br/>                                                                                                                             |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ INSTALLATION \| SHTDN \_ REASON \_ FLAG \_ PLANNED    | "Aplicativo: Instalação (Planejado)" Uma reinicialização planejada ou desligamento para executar a instalação do aplicativo.<br/>                                                                                                                              |
| SHTDN \_ MOTIVO PRINCIPAL DO APLICATIVO \_ \_ \| SHTDN \_ MOTIVO DA \_ MANUTENÇÃO \_ SECUNDÁRIA                                     | "Aplicativo: manutenção (não planejada)" Uma reinicialização ou desligamento não planejado para a manutenção de um aplicativo.<br/>                                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ MAINTENANCE \| SHTDN \_ REASON \_ FLAG \_ PLANNED     | "Aplicativo: Manutenção (Planejado)" Uma reinicialização planejada ou desligamento para executar a manutenção planejada em um aplicativo.<br/>                                                                                                                  |
| SHTDN \_ REASON \_ MAJOR \_ APPLICATION \| SHTDN \_ REASON \_ MINOR \_ UNSTABLE                                        | "Aplicativo: instável" Uma reinicialização ou desligamento não planejado para solucionar problemas de um aplicativo instável.<br/>                                                                                                                                     |
| SHTDN \_ REASON PRINCIPAL HARDWARE \_ \_ \| SHTDN \_ REASON MINOR \_ \_ INSTALLATION                                       | "Hardware: Instalação (não planejado)" Uma reinicialização ou desligamento não planejado para iniciar ou concluir a instalação do hardware.<br/>                                                                                                                     |
| SHTDN \_ REASON PRINCIPAL HARDWARE \_ \_ \| SHTDN \_ REASON MINOR INSTALLATION \_ \_ \| SHTDN \_ REASON FLAG \_ \_ PLANNED       | "Hardware: Instalação (Planejado)" Uma reinicialização planejada ou desligamento para iniciar ou concluir a instalação do hardware.<br/>                                                                                                                          |
| SHTDN MOTIVO PRINCIPAL DE MANUTENÇÃO SECUNDÁRIA \_ DO \_ \_ \| SHTDN \_ MOTIVO DO \_ \_ HARDWARE                                        | "Hardware: manutenção (não planejada)" Uma reinicialização não planejada ou desligamento para o hardware de serviço no sistema.<br/>                                                                                                                               |
| SHTDN \_ MOTIVO PRINCIPAL HARDWARE \_ \_ \| SHTDN \_ MOTIVO \_ \_ \| \_ \_ \_ DA MANUTENÇÃO SECUNDÁRIA SINALIZADOR DE MOTIVO DE MANUTENÇÃO SECUNDÁRIA PLANEJADO        | "Hardware: Manutenção (Planejada)" Uma reinicialização planejada ou desligamento para o hardware de serviço no sistema.<br/>                                                                                                                                    |
| SHTDN \_ REASON PRINCIPAL \_ \_ \_ LEGACY API                                                                          | "Desligamento da API herdada" Esse desligamento foi iniciado pela função [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) herdada. Os aplicativos devem usar [**a função InitiateSystemShutdownEx.**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)<br/> |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ HOTFIX                                      | "Sistema operacional: hot fix (não planejado)" Uma reinicialização ou desligamento não planejado para instalar uma correção de acesso.<br/>                                                                                                                                        |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ HOTFIX \| SHTDN \_ REASON \_ FLAG \_ PLANNED      | "Sistema operacional: hot fix (Planejado)" Uma reinicialização planejada ou desligamento para instalar uma correção de a quente.<br/>                                                                                                                                             |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ RECONFIG                                    | "Sistema operacional: reconfiguração (não planejada)" Uma reinicialização ou desligamento não planejado para alterar a configuração do sistema operacional.<br/>                                                                                                        |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ RECONFIG \| SHTDN \_ REASON \_ FLAG \_ PLANNED    | "Sistema Operacional: Reconfiguração (Planejado)" Uma reinicialização planejada ou desligamento para alterar a configuração do sistema operacional.<br/>                                                                                                             |
| SHTDN \_ MOTIVO \_ PRINCIPAL \_ OPERATINGSYSTEM \| SHTDN \_ REASON MINOR \_ \_ SECURITYFIX                                 | "Sistema operacional: correção de segurança (não planejado)" Uma reinicialização ou desligamento não planejado para instalar um patch de segurança.<br/>                                                                                                                            |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ SECURITYFIX \| SHTDN \_ REASON \_ FLAG \_ PLANNED | "Sistema Operacional: Correção de segurança (Planejado)" Uma reinicialização planejada ou desligamento para instalar um patch de segurança.<br/>                                                                                                                                 |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ SERVICEPACK \| SHTDN \_ REASON \_ FLAG \_ PLANNED | "Sistema operacional: service pack (planejado)" Uma reinicialização planejada ou desligamento para instalar um service pack.<br/>                                                                                                                                   |
| SHTDN \_ REASON \_ MAJOR \_ OPERATINGSYSTEM \| SHTDN \_ REASON \_ MINOR \_ UPGRADE \| SHTDN \_ REASON \_ FLAG \_ PLANNED     | "Sistema Operacional: Atualização (Planejado)" Uma reinicialização planejada ou desligamento para atualizar a configuração do sistema operacional.<br/>                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ OTHER                                                 | "Outros (não planejados)" Um desligamento ou reinicialização não planejado.<br/>                                                                                                                                                                                 |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ OTHER \| SHTDN \_ REASON \_ FLAG \_ PLANNED                 | "Outros (Planejado)" Um desligamento ou reinicialização planejado.<br/>                                                                                                                                                                                      |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ HUNG                                                  | "Outra Falha: Sistema Sem Resposta" O sistema ficou sem resposta.<br/>                                                                                                                                                                  |
| SHTDN \_ REASON \_ MAJOR \_ POWER \| SHTDN \_ REASON \_ MINOR \_ CORDUNPLUGGED                                         | "Falha de energia: Cord Unplugged" O computador foi desconectado.<br/>                                                                                                                                                                           |
| AMBIENTE SECUNDÁRIO DO MOTIVO \_ \_ PRINCIPAL DO POWER \_ \| SHTDN \_ \_ \_                                           | "Falha de energia: ambiente" Houve uma queda de energia.<br/>                                                                                                                                                                                |
| SHTDN \_ REASON \_ MAJOR \_ SYSTEM \| SHTDN \_ REASON \_ MINOR \_ BLUESCREEN                                           | "Falha do sistema: erro de parada" O computador exibiu um evento de falha de tela azul.<br/>                                                                                                                                                        |
| SHTDN \_ MOTIVO PRINCIPAL DO SISTEMA \_ \_ \| SHTDN \_ MOTIVO DA CONECTIVIDADE DE REDE \_ \_ \_ SECUNDÁRIA                                | "Perda de conectividade de rede (não planejada)" O computador precisa ser desligado devido a um problema de conectividade de rede.<br/>                                                                                                                    |
| SHTDN \_ MOTIVO PRINCIPAL DO SISTEMA \_ \_ \| SHTDN \_ MOTIVO SEGURANÇA \_ \_ SECUNDÁRIA                                             | "Problema de segurança" O computador precisa ser desligado devido a um problema de segurança.<br/>                                                                                                                                                          |



 

Você também pode definir seus próprios motivos de desligamento e adicioná-los ao Registro. Cada código de motivo deve ser armazenado como um valor do Registro na seguinte chave:**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Reliability \\ UserDefined \\<default system language \_ \_ \_ ID>**

Essa chave contém nomes de valor da seguinte forma: *xxxxx*; *nnn*; *nnnnn*. Os ponto e vírgulas delimitam os componentes de um nome de valor.

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*Xxxxx*
</dt> <dd>

Um a cinco dos seguintes sinalizadores de controle (nenhum outro caractere pode ser usado).



| Sinalizador | Descrição                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | Desligamento planejado; caso contrário, um desligamento não planejado.                                               |
| C    | Um comentário é necessário. Esse sinalizador deve ser usado com S.<br/>                                  |
| B    | Uma ID é necessária. Esse sinalizador deve ser usado com D.<br/>                                      |
| S    | Exibir a caixa de diálogo de desligamento esperada. S, D ou S e D devem ser usados.<br/>   |
| D    | Exibe a caixa de diálogo desligamento inesperado. S, D ou S e D devem ser usados.<br/> |



 

A ordem na qual os sinalizadores são usados não é importante. Por exemplo, o CSP indica um desligamento planejado em que a caixa de diálogo de desligamento esperada é exibida e um comentário é necessário.

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*Nnn*
</dt> <dd>

Motivo principal. Esse componente deve ser um número no intervalo de 64 a 255. O intervalo de 0 a 63 é reservado para uso pelo sistema.

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*Nnnnn*
</dt> <dd>

Motivo secundário. Esse componente deve estar no intervalo de 0 a 65535.

</dd> </dl>

Os motivos personalizados são classificação na interface do usuário por número de motivo principal e, em seguida, por número de motivo secundário. Não há dois motivos personalizados que possam usar os mesmos motivos principais e secundários, a menos que um esteja planejado e o outro não esteja planejado. Caso contrário, o sistema usará a primeira instância e ignorará as outras.

Os dados de cada valor do Registro são duas cadeias de caracteres, separadas por \\ n \\ r. A primeira cadeia de caracteres é uma cadeia de caracteres de título a ser exibida na caixa de diálogo de desligamento e gravado no log de eventos. O tamanho máximo é de 64 caracteres. As cadeias de caracteres de título devem ser exclusivas. Os títulos personalizados não podem corresponder aos títulos padrão definidos pelo sistema ou a outro título personalizado. A segunda cadeia de caracteres é uma descrição da cadeia de caracteres a ser exibida na caixa de diálogo de desligamento; é opcional. O tamanho máximo é de 256 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Aplicativos de aplicativos de desktop do XP \[ \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2003 \| aplicativo UWP\]<br/>                         |
| Cabeçalho<br/>                   | <dl> <dt>Razão. h</dt> </dl> |



 

 
