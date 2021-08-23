---
description: Indica o motivo pelo qual uma operação WLAN falhou.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (Wlanapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f24b0ab902610408eb7b80b4a962fcc81d4598244714b8f30f0ebf350a7e628
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064556"
---
# <a name="wlan_reason_code"></a>CÓDIGO DE MOTIVO DO WLAN \_ \_

O **tipo \_ WLAN REASON \_ CODE** indica o motivo pelo qual uma operação WLAN falhou.

Você pode usar a [**função WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) para mapear um código de motivo numérico (por exemplo, 0x00050007) para seu significado de texto. Você também pode usar a tabela de pesquisa para ajudar a interpretar o valor numérico do código do motivo. Para exibir a tabela de pesquisa, consulte Apêndice E: Mapeamento de códigos de motivo para mensagens de evento no documento Solução de problemas Windows conexões sem fio do [Vista 802.11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



A tabela a seguir lista códigos de erro gerais.



| Código do motivo                 | Significado                            |
|-----------------------------|------------------------------------|
| WLAN \_ REASON \_ CODE \_ SUCCESS | A operação é bem-sucedida.            |
| CÓDIGO DE \_ MOTIVO \_ WLAN \_ DESCONHECIDO | O motivo da falha é desconhecido. |



 

A tabela a seguir lista os códigos de erro de configuração automática.



| Código de motivo                                  | Significado                                         |
|----------------------------------------------|-------------------------------------------------|
| REDE DE \_ CÓDIGO \_ DE MOTIVO \_ WLAN NÃO \_ \_ COMPATÍVEL | A rede sem fio não é compatível.         |
| PERFIL DE CÓDIGO \_ \_ DO MOTIVO \_ WLAN NÃO \_ \_ COMPATÍVEL | O perfil de rede sem fio não é compatível. |



 

A tabela a seguir lista os códigos de erro de conexão automática.



| Código de motivo                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CÓDIGO DO \_ MOTIVO \_ WLAN \_ SEM CONEXÃO \_ \_ AUTOMÁTICA                   | O perfil não especifica nenhuma conexão automática.                                                                                                                                                                                                                                                                                                                                                                                                               |
| CÓDIGO DE \_ MOTIVO \_ WLAN \_ NÃO \_ VISÍVEL                           | A rede sem fio não está visível.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| GP DE \_ CÓDIGO \_ DE MOTIVO \_ WLAN \_ NEGADO                             | A rede sem fio é bloqueada pela política de grupo.                                                                                                                                                                                                                                                                                                                                                                                                        |
| USUÁRIO DO \_ CÓDIGO \_ DO MOTIVO \_ WLAN \_ NEGADO                           | A rede sem fio é bloqueada pelo usuário.                                                                                                                                                                                                                                                                                                                                                                                                            |
| TIPO \_ \_ BSS DE CÓDIGO DE \_ MOTIVO WLAN \_ NÃO \_ \_ PERMITIDO                | O tipo BSS (conjunto de serviços básico) não é permitido neste adaptador sem fio.                                                                                                                                                                                                                                                                                                                                                                               |
| CÓDIGO DO MOTIVO DO WLAN \_ \_ NA LISTA DE \_ \_ \_ FALHAS                       | A rede sem fio está na lista com falha.                                                                                                                                                                                                                                                                                                                                                                                                             |
| CÓDIGO DO MOTIVO DO WLAN \_ \_ NA LISTA \_ \_ BLOQUEADA \_                      | A rede sem fio está na lista bloqueada.                                                                                                                                                                                                                                                                                                                                                                                                            |
| LISTA SSID DO CÓDIGO \_ \_ DE MOTIVO \_ WLAN MUITO \_ \_ \_ LONGA                  | O tamanho da lista de SSID (identificadores do conjunto de serviços) excede o tamanho máximo com suporte do adaptador.                                                                                                                                                                                                                                                                                                                                                  |
| FALHA NA \_ CHAMADA DE CONEXÃO DO CÓDIGO DO MOTIVO \_ \_ \_ DO \_ WLAN                    | Falha na chamada de conexão do MSM (Módulo Específico de Mídia).                                                                                                                                                                                                                                                                                                                                                                                                     |
| FALHA NA \_ CHAMADA DE VERIFICAÇÃO DE CÓDIGO DO MOTIVO \_ \_ \_ DO \_ WLAN                       | A chamada de verificação do MSM falha.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| REDE DE \_ CÓDIGO \_ DE MOTIVO \_ WLAN NÃO \_ \_ DISPONÍVEL                | A rede especificada não está disponível. Esse código de motivo também é usado quando há uma incompatibilidade entre os recursos especificados em um perfil XML e recursos de interface e/ou rede. Por exemplo, se um perfil especificar o uso de WPA2 quando a NIC só dá suporte a WPA, esse código de erro será retornado. Além disso, se um perfil especificar o uso do modo FIPS quando a NIC não dá suporte ao modo FIPS, esse código de erro será retornado.<br/> |
| PERFIL DE CÓDIGO DO MOTIVO DO WLAN \_ \_ ALTERADO OU \_ \_ \_ \_ EXCLUÍDO          | O perfil foi alterado ou excluído antes da conexão ser estabelecida.                                                                                                                                                                                                                                                                                                                                                                               |
| INCOMPATIBILIDADE DA CHAVE DE \_ \_ CÓDIGO DO MOTIVO \_ \_ DO WLAN                          | A chave de perfil não é igual à chave de rede.                                                                                                                                                                                                                                                                                                                                                                                                         |
| O USUÁRIO DO CÓDIGO DO MOTIVO DO WLAN \_ \_ NÃO \_ \_ \_ RESPONDE                     | O usuário não está respondendo.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| PERFIL DE \_ AP DE CÓDIGO DO MOTIVO \_ \_ WLAN NÃO PERMITIDO \_ PARA O \_ \_ \_ \_ CLIENTE | Um aplicativo tentou aplicar um perfil de Rede Hospedada sem fio a um adaptador de rede sem fio físico usando a [**função WlanSetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) em vez de um dispositivo virtual.                                                                                                                                                                                                                                                    |
| PERFIL DE \_ AP DE CÓDIGO DE MOTIVO \_ \_ WLAN NÃO \_ \_ \_ PERMITIDO              | Um aplicativo tentou aplicar um perfil de Rede Hospedada sem fio a um adaptador de rede sem fio físico usando a [**função WlanSetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) em vez de um dispositivo virtual.                                                                                                                                                                                                                                                    |



 

A tabela a seguir lista os códigos de erro de validação de perfil.



| Código de motivo                                                    | Significado                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ESQUEMA DE PERFIL INVÁLIDO DO CÓDIGO DO MOTIVO \_ \_ \_ \_ \_ WLAN                   | O perfil inválido de acordo com o esquema.                                                                                                                                                                                                  |
| PERFIL DE CÓDIGO \_ \_ DO MOTIVO WLAN \_ \_ AUSENTE                           | O elemento WLANProfile está ausente.                                                                                                                                                                                                           |
| NOME DE PERFIL \_ \_ INVÁLIDO DO CÓDIGO \_ DO MOTIVO \_ \_ DO WLAN                     | O nome do perfil é inválido.                                                                                                                                                                                                           |
| TIPO DE PERFIL INVÁLIDO DO CÓDIGO DO MOTIVO \_ \_ \_ \_ \_ WLAN                     | O tipo do perfil é inválido.                                                                                                                                                                                                           |
| TIPO \_ PHY INVÁLIDO DO CÓDIGO \_ DE MOTIVO \_ \_ WLAN \_                         | O tipo PHY é inválido.                                                                                                                                                                                                                      |
| WLAN \_ REASON \_ CODE \_ MSM \_ SECURITY \_ MISSING                     | As configurações de segurança do MSM estão ausentes.                                                                                                                                                                                                        |
| NÃO HÁ \_ SUPORTE PARA A SEGURANÇA DE \_ \_ IHV \_ \_ DO \_ CÓDIGO DO MOTIVO WLAN              | As configurações de segurança de IHV (fornecedor independente de hardware) estão ausentes.                                                                                                                                                                          |
| INCOMPATIBILIDADE DE \_ \_ \_ IHV \_ OUI DO CÓDIGO DE MOTIVO WLAN \_                         | A UOI do perfil IHV não foi igual à UOI do adaptador.                                                                                                                                                                                       |
| CÓDIGO DE \_ MOTIVO \_ \_ WLAN IHV \_ OUI \_ AUSENTE                          | As configurações de UOI de IHV estão ausentes.                                                                                                                                                                                                             |
| CONFIGURAÇÕES \_ DE \_ \_ IHV DO CÓDIGO DO MOTIVO WLAN \_ \_ AUSENTES                     | As configurações de segurança de IHV estão ausentes.                                                                                                                                                                                                        |
| CONECTIVIDADE \_ \_ \_ IHV DO \_ CÓDIGO DO \_ \_ MOTIVO WLAN SEM SUPORTE          | Um aplicativo tentou aplicar um perfil IHV em um adaptador que não dá suporte a configurações de conectividade IHV.                                                                                                                                   |
| SEGURANÇA DE CONFLITO DE CÓDIGO \_ \_ DO MOTIVO \_ DO \_ WLAN                         | O conflito de configurações de segurança.                                                                                                                                                                                                               |
| SEGURANÇA DE CÓDIGO DO MOTIVO DO WLAN \_ \_ \_ \_ AUSENTE                          | As configurações de segurança estão ausentes.                                                                                                                                                                                                            |
| TIPO \_ \_ \_ \_ BSS INVÁLIDO DO CÓDIGO DE MOTIVO WLAN \_                         | O tipo BSS não é válido.                                                                                                                                                                                                                    |
| MODO DE CONEXÃO \_ \_ \_ ADHOC INVÁLIDO DO CÓDIGO DE MOTIVO \_ \_ \_ WLAN           | A conexão automática não pode ser definida para uma rede ad hoc.                                                                                                                                                                                     |
| WLAN \_ REASON \_ CODE \_ NON \_ BROADCAST \_ SET \_ FOR \_ ADHOC            | Não é possível definir a não difusão para uma rede ad hoc.                                                                                                                                                                                            |
| CONJUNTO DE COMUTROS AUTOMÁTICOS DO CÓDIGO DO MOTIVO DO WLAN \_ \_ PARA \_ \_ \_ \_ \_ ADHOC              | A opção automática não pode ser definida para uma rede ad hoc.                                                                                                                                                                                              |
| CONJUNTO DE COMUTAMENTO AUTOMÁTICO DO CÓDIGO DO MOTIVO DO WLAN \_ \_ PARA CONEXÃO \_ \_ \_ \_ \_ \_ MANUAL | Não é possível definir a opção automática para um perfil de conexão manual.                                                                                                                                                                                    |
| CÓDIGO DO MOTIVO DO WLAN \_ \_ \_ \_ ONEX SECURITY \_ ONEX \_ AUSENTE               | As configurações de segurança do IHV 802.1X estão ausentes.                                                                                                                                                                                                 |
| SSID DO PERFIL DE CÓDIGO DO MOTIVO DO WLAN \_ \_ \_ \_ \_ INVÁLIDO                     | O SSID no perfil é inválido ou está ausente.                                                                                                                                                                                                |
| código de motivo da WLAN número \_ \_ excessivo de \_ \_ \_ SSID                            | Muitos SSIDs foram especificados no perfil.                                                                                                                                                                                                 |
| motivo da WLAN \_ \_ código de conectividade do \_ IHV \_ \_ não \_ suportado          |                                                                                                                                                                                                                                               |
| \_ \_ código de motivo \_ \_ da WLAN \_ número máximo de clientes inválidos \_ \_ \_ para \_ AP     | Um aplicativo tentou aplicar um perfil de rede hospedada sem fio a uma NIC de adaptador de rede física usando a função [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) e especificou um valor inaceitável para o número máximo de clientes permitido. |
| código de motivo da WLAN \_ \_ \_ \_ canal inválido                           | O canal especificado é inválido.                                                                                                                                                                                                             |
| modo de operação de código de motivo de WLAN \_ \_ \_ \_ \_ sem \_ suporte            |                                                                                                                                                                                                                                               |
| \_perfil de AP automático de código de motivo de WLAN \_ \_ \_ \_ \_ não \_ permitido            | Ocorreu um erro interno do sistema operacional com a rede hospedada sem fio.                                                                                                                                                                 |
| a \_ conexão automática do código de motivo da WLAN \_ \_ não é \_ \_ \_ permitida             |                                                                                                                                                                                                                                               |



 

A tabela a seguir lista os códigos de erro de incompatibilidade de rede MSM.



| Código de motivo                                            | Significado                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| \_código de motivo da WLAN \_ \_ \_ com segurança sem suporte \_ definido \_ pelo \_ sistema operacional | As configurações de segurança não são suportadas pelo sistema operacional. |
| código de motivo da WLAN com o \_ \_ \_ conjunto de segurança sem suporte \_ \_         | Não há suporte para as configurações de segurança.                         |
| tipo de BSS do código do motivo da WLAN sem \_ \_ \_ \_ \_ correspondência                 | O tipo de BSS não corresponde.                                     |
| código de motivo da WLAN \_ \_ \_ tipo PHY sem \_ \_ correspondência                 | O tipo PHY não corresponde.                                     |
| incompatibilidade de código de motivo de WLAN \_ \_ \_ \_                  | A taxa de dados não corresponde.                                    |



 

A tabela a seguir lista os códigos de erro de falha de conexão MSM.



| Código de motivo                                       | Significado                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| código de motivo da WLAN \_ \_ \_ usuário \_ cancelado               | O usuário cancelou a operação.                                                                             |
| \_falha de \_ Associação de código do motivo da WLAN \_ \_          | Driver desconectado ao associar.                                                                       |
| \_ \_ \_ tempo limite de associação de código de motivo de WLAN \_          | A associação atingiu o tempo limite.                                                                                       |
| \_falha de \_ pré \_ - \_ segurança do código \_ de motivo da WLAN        | Falha na segurança da pré-associação.                                                                            |
| \_erro de \_ segurança ao iniciar o código de motivo da \_ \_ WLAN \_      | Falha ao iniciar a segurança após a associação.                                                                  |
| \_falha de \_ segurança do código de motivo da WLAN \_ \_             | A segurança acaba com falhas.                                                                               |
| \_ \_ \_ tempo limite de segurança do código de motivo da WLAN \_             | A operação de segurança atinge o tempo limite.                                                                                |
| \_falha de \_ roaming de código de motivo da WLAN \_ \_              | Driver desconectado durante roaming.                                                                           |
| motivo da WLAN \_ \_ falha de \_ segurança de roaming de código \_ \_    | Falha ao iniciar a segurança para roaming.                                                                        |
| código de motivo da WLAN \_ \_ \_ falha de \_ segurança adhoc \_      | Falha ao iniciar a segurança para o par ad hoc.                                                                    |
| Driver de código de motivo da WLAN \_ \_ \_ \_ desconectado          | Driver desconectado.                                                                                         |
| \_ \_ \_ \_ falha na operação do driver de código de motivo \_ da WLAN    | Falha do driver ao executar algumas operações.                                                                    |
| código de motivo da WLAN \_ \_ \_ \_ não disponível para IHV \_           | O serviço IHV não está disponível.                                                                            |
| motivo de WLAN \_ \_ código \_ IHV \_ não \_ respondendo          | A resposta do serviço IHV atingiu o tempo limite.                                                                 |
| \_ \_ \_ tempo limite de desconexão do código de motivo da WLAN \_           | Tempo limite excedido aguardando a desconexão do driver.                                                              |
| \_ \_ falha interna do código de motivo da \_ WLAN \_             | Um erro interno impediu a conclusão da operação.                                              |
| \_motivo \_ da WLAN \_ código \_ \_ tempo limite da solicitação da interface do usuário          | Uma solicitação de interação do usuário atingiu o tempo limite.                                                                        |
| código de motivo da WLAN \_ \_ \_ \_ muitas \_ tentativas de segurança \_ | Roaming com muita frequência. A segurança de postagem não foi concluída após 5 tentativas.                                         |
| código de motivo da WLAN \_ \_ erro ao iniciar a \_ \_ \_ falha         | Ocorreu um erro interno do sistema operacional que resultou em uma falha ao iniciar a rede hospedada sem fio. |



 

A tabela a seguir lista os códigos de erro de segurança do MSM.



| Código de motivo                                                             | Significado                                                                                                                                                                                   |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de \_ \_ chave inválido \_                | O índice de chave especificado não é válido.                                                                                                                                                         |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ PSK \_ presente                       | Chave necessária, PSK presente.                                                                                                                                                                |
| código de motivo da WLAN \_ \_ MSMSEC de \_ \_ chave do perfil \_ \_                        | Comprimento de chave inválido.                                                                                                                                                                       |
| código de motivo de WLAN \_ \_ MSMSEC do \_ \_ perfil \_ PSK \_ comprimento                        | Comprimento PSK inválido.                                                                                                                                                                       |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ sem \_ codificação de autenticação \_ \_ especificada        | Nenhum par de auth/Cipher especificado.                                                                                                                                                           |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de autenticação em \_ excesso número de \_ \_ \_ criptografia \_ especificado | Muitos pares de auth/Cipher especificados.                                                                                                                                                     |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ autenticação duplicada \_ \_ codificação            | O perfil contém um par de autenticação/codificação duplicado.                                                                                                                                              |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ RAWDATA \_ inválido                   | Os dados brutos do perfil são inválidos.                                                                                                                                                              |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de \_ \_ autenticação inválido \_              | Combinação de autenticação/codificação inválida.                                                                                                                                                          |
| código de motivo da WLAN \_ \_ MSMSEC do \_ \_ perfil \_ Onex \_ desabilitado                     | 802.1 x desabilitado quando é necessário habilitá-lo.                                                                                                                                        |
| código de motivo da WLAN \_ \_ MSMSEC do \_ \_ perfil \_ 802.1x \_ habilitado                      | 802.1 x habilitado quando ele precisa ser desabilitado.                                                                                                                                        |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ \_ modo de PMKCACHE inválido \_            | Modo de cache PMK inválido.                                                                                                                                                                   |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ \_ PMKCACHE \_ tamanho inválido            | Tamanho do cache PMK inválido.                                                                                                                                                                   |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ \_ PMKCACHE \_ TTL inválido             | TTL de cache PMK inválido.                                                                                                                                                                    |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ \_ modo de PreAuth inválido \_             | Modo de PreAuth inválido.                                                                                                                                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ INVALID \_ PREAUTH \_ THROTTLE         | Aceleração de pré-auidade inválida.                                                                                                                                                                 |
| \_PREAUTH DO PERFIL DO \_ \_ MSMSEC \_ DO \_ \_ \_ CÓDIGO DO MOTIVO WLAN HABILITADO SOMENTE             | Pré-auth habilitado quando o cache PMK está desabilitado.                                                                                                                                               |
| REDE DE \_ \_ \_ FUNCIONALIDADES MSMSEC DO CÓDIGO \_ DO MOTIVO WLAN \_                         | Falha na correspondência de funcionalidades na rede.                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ NIC                             | Falha na correspondência de funcionalidades na NIC.                                                                                                                                                        |
| PERFIL DE FUNCIONALIDADE \_ \_ \_ MSMSEC DO CÓDIGO \_ DO MOTIVO WLAN \_                         | Falha na correspondência de funcionalidades no perfil.                                                                                                                                                    |
| DESCOBERTA DE FUNCIONALIDADE \_ \_ DO \_ MSMSEC DO CÓDIGO \_ DO MOTIVO WLAN \_                       | A rede não dá suporte ao tipo de funcionalidade especificado.                                                                                                                                       |
| CÓDIGO DO MOTIVO WLAN FRASE-CHAVE DO PERFIL \_ \_ \_ MSMSEC \_ \_ \_ CHAR                   | A frase-senha contém caractere inválido.                                                                                                                                                    |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEYMATERIAL \_ CHAR                  | O material da chave contém caractere inválido.                                                                                                                                                  |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ WRONG \_ KEYTYPE                     | O tipo de chave especificado não combina com o material da chave.                                                                                                                                   |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ MIXED \_ CELL                                 | Suspeita-se de uma célula mista. A AP não está sinalizando que é compatível com um perfil habilitado para privacidade.                                                                                  |
| TEMPORIZADORES DE \_ \_ AUTH DO PERFIL \_ MSMSEC DO CÓDIGO DO MOTIVO WLAN \_ \_ \_ \_ INVÁLIDOS              | O número de temporizadores de autenticação ou o número de tempos máximos especificados no perfil é inválido.                                                                                        |
| WLAN \_ REASON CODE PERFIL \_ \_ MSMSEC \_ INVALID \_ \_ GKEY \_ INTV                | O intervalo de atualização de chave de grupo especificado no perfil é inválido.                                                                                                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ TRANSITION \_ NETWORK                         | Suspeita-se de uma "rede de transição". A segurança herdada 802.11 é usada para a próxima tentativa de autenticação.                                                                                  |
| CÓDIGO DO \_ MOTIVO WLAN \_ CHAVE DE PERFIL \_ MSMSEC \_ NÃO \_ \_ \_ MAPEADA CHAR                | A chave contém caracteres que não estão no conjunto de caracteres ASCII.                                                                                                                      |
| AUTH DO PERFIL \_ \_ DE FUNCIONALIDADE DO \_ MSMSEC \_ DO \_ \_ CÓDIGO DO MOTIVO WLAN                   | Falha na correspondência de funcionalidades porque a rede não dá suporte ao método de autenticação no perfil.                                                                                 |
| CODIFICAÇÃO DO PERFIL \_ \_ DE FUNCIONALIDADE DO \_ MSMSEC \_ DO \_ \_ CÓDIGO DO MOTIVO WLAN                 | Falha na correspondência de funcionalidades porque a rede não dá suporte ao algoritmo de criptografia no perfil.                                                                                      |
| MODO DE SEGURANÇA DO PERFIL \_ \_ DO \_ MSMSEC DO CÓDIGO \_ \_ \_ DO MOTIVO WLAN                         | O valor do modo FIPS 140-2 no perfil é inválido.                                                                                                                                          |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ SAFE \_ MODE \_ NIC        | O perfil requer o modo FIPS 140-2, que não é suportado pela placa de interface de rede (NIC).                                                                                                 |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ PROFILE \_ SAFE \_ MODE \_ NW         | O perfil requer o modo FIPS 140-2, que não é suportado pela rede.                                                                                                                      |
| AUTH SEM SUPORTE DO PERFIL \_ \_ \_ MSMSEC \_ \_ DO \_ CÓDIGO DO MOTIVO WLAN                  | O perfil especifica um mecanismo de autenticação sem suporte.                                                                                                                               |
| CODIFICAÇÃO SEM SUPORTE DO \_ \_ PERFIL \_ MSMSEC \_ \_ \_ DO CÓDIGO DO MOTIVO WLAN                | O perfil especifica uma codificação sem suporte.                                                                                                                                                  |
| FALHA NA SOLICITAÇÃO DA \_ INTERFACE DO USUÁRIO do \_ \_ MSMSEC \_ DO \_ \_ CÓDIGO DO MOTIVO WLAN                        | Falha ao enfilfilar a solicitação de interface do usuário.                                                                                                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ MFP \_ NW \_ NIC                    | A LAN sem fio requer o MFP (Management Frame Protection) e o interface de rede não dá suporte ao MFP. Para obter mais informações, consulte o alteração IEEE 802.11w para o padrão 802.11. |



 

A tabela a seguir lista os códigos de erro de conexão do MSM.



| Código de motivo                                             | Significado                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ AUTH \_ START \_ TIMEOUT        | A autenticação 802.1X não foi iniciada dentro do tempo configurado.                                                      |
| TEMPOOUT DE SUCESSO \_ \_ DA \_ \_ AUTH DO MSMSEC DO \_ \_ CÓDIGO DO MOTIVO WLAN      | A autenticação 802.1X não foi concluída no tempo configurado.                                                   |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ KEY \_ START \_ TIMEOUT         | A troca dinâmica de chaves não começou dentro do tempo configurado.                                                       |
| TEMPO DE SUCESSO DA \_ \_ CHAVE \_ MSMSEC \_ DO \_ \_ CÓDIGO DO MOTIVO WLAN       | A troca dinâmica de chaves não foi concluída dentro do tempo configurado.                                                    |
| DADOS DE CHAVE \_ \_ \_ AUSENTES DO MSMSEC \_ M3 \_ \_ DO \_ CÓDIGO DO MOTIVO DO WLAN      | A mensagem 3 do handshake de 4 vias não tem dados de chave.                                                                    |
| CÓDIGO DO \_ MOTIVO \_ WLAN \_ MSMSEC \_ M3 \_ AUSENTE \_ IE             | A mensagem 3 do handshake de 4 vias não tem IE.                                                                          |
| CÓDIGO DO \_ MOTIVO \_ WLAN \_ MSMSEC \_ M3 \_ CHAVE \_ GRP \_ AUSENTE       | A mensagem 3 do handshake de 4 vias não tem nenhuma chave GRP.                                                                     |
| CORRESPONDÊNCIA DE IE DE PR DO \_ \_ \_ MSMSEC DO CÓDIGO DE MOTIVO \_ \_ WLAN \_            | Falha na correspondência dos recursos de segurança do IE na M3.                                                               |
| CORRESPONDÊNCIA DE CÓDIGO \_ DE \_ MOTIVO \_ WLAN MSMSEC \_ SEC \_ \_ IE           | Falha na correspondência das funcionalidades de segurança do IE secundário no M3.                                                     |
| CÓDIGO DE \_ MOTIVO \_ WLAN \_ MSMSEC \_ SEM CHAVE \_ \_ EMPARELHADA           | Era necessária uma chave emparelhada, mas o AP (ponto de acesso) configurava apenas as chaves de grupo.                                        |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ G1 \_ MISSING \_ KEY \_ DATA      | A mensagem 1 do handshake de chave de grupo não tem dados de chave.                                                                |
| CHAVE GRP AUSENTE DO CÓDIGO DO MOTIVO \_ \_ \_ WLAN MSMSEC \_ \_ \_ G1 \_       | A mensagem 1 do handshake de chave de grupo não tem nenhuma chave de grupo.                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PEER \_ INDICATED \_ INSECURE   | O bit seguro de redefinição de AP foi redefinido depois que a conexão foi protegida.                                                                |
| CÓDIGO DE \_ MOTIVO \_ WLAN \_ MSMSEC \_ SEM \_ AUTENTICADOR           | 802.1X indicou que não há nenhum autenticador, mas o perfil requer um.                                   |
| FALHA NA \_ \_ \_ NIC DO MSMSEC DO CÓDIGO \_ DO MOTIVO WLAN \_                | Falha nas configurações de canalização para NIC.                                                                                 |
| CÓDIGO \_ DE MOTIVO \_ WLAN \_ MSMSEC \_ CANCELADO                   | A operação foi cancelada por um chamador.                                                                              |
| FORMATO DE CHAVE \_ \_ \_ MSMSEC DO CÓDIGO DO MOTIVO \_ \_ WLAN                 | O formato de chave inserido não está em um formato válido.                                                                     |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ DOWNGRADE \_ DETECTED         | Foi detectado um downgrade de segurança.                                                                               |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ PSK \_ MISMATCH \_ SUSPECTED    | Suspeita de incompatibilidade de PSK.                                                                                     |
| FALHA FORÇADA DO \_ \_ \_ MSMSEC NO \_ CÓDIGO DO MOTIVO WLAN \_             | Houve uma falha forçada porque o método de conexão não era seguro.                                         |
| CÓDIGO \_ DE MOTIVO \_ WLAN \_ MSMSEC \_ M3 \_ MUITO \_ \_ RSRIA        | A mensagem 3 de handshake de 4 maneiras contém muito RSN (IE RSN).                                                     |
| DADOS DE CHAVE \_ \_ \_ AUSENTES DO MSMSEC \_ M2 \_ \_ DO \_ CÓDIGO DO MOTIVO DO WLAN      | A mensagem 2 do handshake de 4 vias não tem nenhum dado de chave (Adhoc do RSN).                                                        |
| CÓDIGO DO \_ MOTIVO \_ WLAN \_ MSMSEC \_ M2 \_ AUSENTE \_ IE             | A mensagem 2 do handshake de 4 vias não tem IE (RSN Adhoc).                                                              |
| WLAN \_ REASON \_ CODE \_ MSMSEC \_ AUTH \_ WCN \_ COMPLETED        |                                                                                                                  |
| FALHA NA INTERFACE DO USUÁRIO DE \_ \_ SEGURANÇA DO \_ MSMSEC \_ DO \_ \_ CÓDIGO DO MOTIVO WLAN       | A solicitação de interface do usuário de segurança falhou porque a solicitação não pôde ser en fila ou porque o usuário cancelou a solicitação. |
| CÓDIGO DO \_ MOTIVO \_ WLAN \_ MSMSEC \_ M3 \_ CHAVE \_ \_ GRP \_ AUSENTE | A mensagem 3 do handshake de 4 vias não tem nenhuma RSN (Chave de Grupo Mgmt).                                                        |
| CÓDIGO DO \_ MOTIVO \_ WLAN \_ MSMSEC \_ G1 \_ CHAVE \_ \_ GRP AUSENTE \_ | A mensagem 1 do handshake de chave de grupo não tem nenhuma chave de gerenciamento de grupo.                                                    |



 

A tabela a seguir lista os códigos de motivo 802.1X. Os elementos de esquema nomeados abaixo são definidos no esquema OneX e especificados no perfil WLAN.



| Código de motivo                                         | Significado                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O ONEX \_ NÃO CONSEGUE IDENTIFICAR O \_ \_ \_ USUÁRIO                    | Nenhum usuário está disponível para autenticação 802.1X. Esse erro pode ocorrer quando a autenticação do computador está desabilitada e nenhum usuário está conectado ao computador.                              |
| IDENTIDADE ONEX \_ \_ NÃO \_ ENCONTRADA                          | Não foi possível encontrar a identidade 802.1X.                                                                                                                                            |
| INTERFACE DO \_ USUÁRIO ONEX \_ DESABILITADA                                  | A autenticação só pôde ser concluída por meio da interface do usuário e essa interface não pôde ser exibida.                                                                       |
| FALHA DE \_ EAP \_ ONEX \_ RECEBIDA                        | Falha na autenticação de EAP.                                                                                                                                                     |
| ONEX \_ AUTHENTICATOR \_ NÃO ESTÁ \_ MAIS \_ PRESENTE            | O autenticador 802.1X saiu da rede.                                                                                                                               |
| VERSÃO DO \_ PERFIL \_ ONEX \_ SEM \_ SUPORTE              | Não há suporte para a versão do perfil OneX fornecido.                                                                                                                         |
| TAMANHO INVÁLIDO \_ DO PERFIL \_ ONEX \_                      | O perfil OneX tem um comprimento inválido.                                                                                                                                            |
| TIPO DE \_ EAP DE PERFIL ONEX \_ \_ NÃO \_ PERMITIDO                | O tipo EAP especificado no perfil OneX (possivelmente fornecido pelo elemento EAPType) não é permitido.                                                                               |
| TIPO OU \_ \_ SINALIZADOR DE \_ EAP INVÁLIDO DO \_ \_ \_ PERFIL ONEX         | O Tipo de EAP especificado no perfil OneX (possivelmente fornecido pelo elemento EAPType) é inválido ou um dos sinalizadores EAP (possivelmente fornecidos no elemento EAPConfig) é inválido. |
| SINALIZADORES \_ \_ \_ ONEX \_ INVÁLIDOS DO PERFIL ONEX                 | Os sinalizadores flexíveis (possivelmente fornecidos no elemento EAPConfig) no perfil OneX são inválidos.                                                                                 |
| VALOR DE \_ \_ TEMPORIZADOR INVÁLIDO DO PERFIL \_ ONEX \_                | Um temporizador especificado no perfil OneX (possivelmente fornecido pelo elemento heldPeriod, authPeriod ou startPeriod) é inválido.                                                        |
| MODO DE \_ \_ \_ SUPPLICANT \_ INVÁLIDO DO PERFIL ONEX            | O modo flexível especificado no perfil OneX (possivelmente fornecido pelo elemento supplicantMode) é inválido.                                                                    |
| MODO DE \_ \_ \_ AUTH INVÁLIDO DO PERFIL \_ ONEX                  | O modo de autenticação especificado no perfil OneX (possivelmente fornecido pelo elemento authMode) é inválido.                                                                      |
| PROPRIEDADES DE \_ CONEXÃO \_ DE \_ EAP INVÁLIDAS \_ DO PERFIL ONEX \_ | As propriedades de conexão especificadas no perfil OneX (possivelmente fornecidas pelo elemento EAPConfig) são inválidas.                                                                  |



 

## <a name="remarks"></a>Comentários

Há suporte para um conjunto limitado de códigos de motivo no Windows XP com Service Pack 3 (SP3) e na API de LAN sem fio para Windows XP com Service Pack 2 (SP2). Os códigos de erro de validação de perfil com suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2 são os exemplos a seguir:

-   ESQUEMA DE PERFIL INVÁLIDO DO CÓDIGO DO MOTIVO \_ \_ \_ \_ \_ WLAN
-   PERFIL DE CÓDIGO \_ \_ DO MOTIVO WLAN \_ \_ AUSENTE
-   SSID DO PERFIL DE CÓDIGO DO MOTIVO DO WLAN \_ \_ \_ \_ \_ INVÁLIDO

Os códigos de erro de segurança do MSM com suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2 são os exemplos a seguir:

-   ÍNDICE DE CHAVE \_ INVÁLIDO \_ DO PERFIL \_ MSMSEC \_ DO \_ \_ \_ CÓDIGO DO MOTIVO WLAN
-   COMPRIMENTO DA CHAVE DO PERFIL \_ \_ \_ MSMSEC DO CÓDIGO DO MOTIVO \_ \_ WLAN \_
-   COMPRIMENTO \_ PSK DO PERFIL \_ \_ MSMSEC DO CÓDIGO DO MOTIVO \_ \_ WLAN \_
-   CODIFICAÇÃO DE \_ \_ \_ \_ \_ \_ AUTH INVÁLIDA DO PERFIL MSMSEC DO CÓDIGO \_ DE MOTIVO WLAN
-   CÓDIGO DO MOTIVO WLAN \_ \_ PERFIL \_ MSMSEC \_ \_ ONEX \_ DESABILITADO
-   CÓDIGO DO \_ MOTIVO \_ WLAN \_ PERFIL MSMSEC \_ \_ ONEX \_ HABILITADO
-   REDE DE \_ \_ \_ FUNCIONALIDADES MSMSEC DO CÓDIGO \_ DO MOTIVO WLAN \_
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ CAPABILITY \_ NIC
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ KEYMATERIAL \_ CHAR
-   WLAN \_ REASON \_ CODE \_ MSMSEC \_ PROFILE \_ WRONG \_ KEYTYPE

Os códigos de erro 802.1x com suporte no Windows XP com SP3 e na API de LAN Sem Fio para Windows XP com SP2 são os exemplos a seguir:

-   TAMANHO INVÁLIDO \_ DO PERFIL \_ ONEX \_
-   TIPO OU \_ \_ SINALIZADOR DE \_ EAP INVÁLIDO DO \_ \_ \_ PERFIL ONEX
-   MODO DE \_ \_ \_ AUTH INVÁLIDO DO PERFIL \_ ONEX
-   PROPRIEDADES DE \_ CONEXÃO \_ DE \_ EAP INVÁLIDAS \_ DO PERFIL ONEX \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows XP somente com aplicativos da área de trabalho SP3 \[\]<br/>                  |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wlanapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
