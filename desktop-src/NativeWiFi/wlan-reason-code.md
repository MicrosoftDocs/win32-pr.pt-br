---
description: Indica o motivo pelo qual uma operação de WLAN falhou.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (wlanapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba0ae705244541063564431809cffa953a0f3fd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506231"
---
# <a name="wlan_reason_code"></a>\_código de motivo da WLAN \_

O tipo de **\_ \_ código de motivo da WLAN** indica o motivo da falha de uma operação de WLAN.

Você pode usar a função [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) para mapear um código de motivo numérico (por exemplo, 0x00050007) para seu significado de texto. Você também pode usar a tabela de pesquisa para ajudar a interpretar o valor numérico do código de motivo. Para exibir a tabela de pesquisa, consulte o Apêndice E: mapeamento de códigos de motivo para mensagens de evento no documento [solução de problemas de conexões sem fio do Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



A tabela a seguir lista os códigos de erro gerais.



| Código do motivo                 | Significado                            |
|-----------------------------|------------------------------------|
| código do motivo da WLAN com \_ \_ \_ êxito | A operação é realizada com sucesso.            |
| código de motivo de WLAN \_ \_ \_ desconhecido | O motivo da falha é desconhecido. |



 

A tabela a seguir lista os códigos de erro de configuração automática.



| Código de motivo                                  | Significado                                         |
|----------------------------------------------|-------------------------------------------------|
| código de motivo da WLAN \_ \_ \_ rede \_ \_ incompatível | A rede sem fio não é compatível.         |
| Perfil de código de motivo da WLAN \_ \_ \_ \_ não \_ compatível | O perfil de rede sem fio não é compatível. |



 

A tabela a seguir lista os códigos de erro de conexão automática.



| Código de motivo                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| código de motivo da WLAN \_ \_ \_ sem \_ \_ conexão automática                   | O perfil não especifica conexão automática.                                                                                                                                                                                                                                                                                                                                                                                                               |
| código de motivo da WLAN \_ \_ \_ não \_ visível                           | A rede sem fio não está visível.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| código de motivo da WLAN \_ \_ \_ GP \_ negado                             | A rede sem fio está bloqueada pela política de grupo.                                                                                                                                                                                                                                                                                                                                                                                                        |
| código de motivo da WLAN \_ \_ \_ \_ negado pelo usuário                           | A rede sem fio está bloqueada pelo usuário.                                                                                                                                                                                                                                                                                                                                                                                                            |
| tipo de BSS do código de motivo da WLAN \_ \_ \_ \_ \_ não \_ permitido                | O tipo de BSS (conjunto de serviços básico) não é permitido neste adaptador sem fio.                                                                                                                                                                                                                                                                                                                                                                               |
| \_ \_ código de motivo \_ da WLAN na \_ lista de falhas \_                       | A rede sem fio está na lista de falhas.                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ código de motivo \_ da WLAN na \_ lista de bloqueios \_                      | A rede sem fio está na lista de bloqueios.                                                                                                                                                                                                                                                                                                                                                                                                            |
| código de motivo da WLAN \_ \_ lista de \_ SSID \_ \_ muito \_ longa                  | O tamanho da lista de SSIDs (identificadores de conjunto de serviços) excede o tamanho máximo suportado pelo adaptador.                                                                                                                                                                                                                                                                                                                                                  |
| motivo da WLAN \_ \_ código \_ \_ falha ao chamar chamada \_                    | A chamada de conexão do módulo específico de mídia (MSM) falha.                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_ \_ \_ \_ falha na chamada de exame de código de motivo \_ da WLAN                       | A chamada de verificação de MSM falha.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| rede de código de motivo da WLAN \_ \_ \_ \_ não \_ disponível                | A rede especificada não está disponível. Esse código de motivo também é usado quando há uma incompatibilidade entre os recursos especificados em um perfil XML e os recursos de interface e/ou rede. Por exemplo, se um perfil especifica o uso de WPA2 quando a NIC só dá suporte a WPA, esse código de erro é retornado. Além disso, se um perfil especificar o uso do modo FIPS quando a NIC não oferecer suporte ao modo FIPS, esse código de erro será retornado.<br/> |
| \_ \_ \_ perfil \_ de código de motivo de WLAN alterado \_ ou \_ excluído          | O perfil foi alterado ou excluído antes da conexão ser estabelecida.                                                                                                                                                                                                                                                                                                                                                                               |
| incompatibilidade de chave de código de \_ motivo de WLAN \_ \_ \_                          | A chave de perfil não corresponde à chave de rede.                                                                                                                                                                                                                                                                                                                                                                                                         |
| motivo da WLAN o \_ \_ usuário do código \_ \_ não \_ responde                     | O usuário não está respondendo.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ \_ perfil AP de código \_ \_ de motivo de WLAN não \_ permitido \_ para \_ cliente | Um aplicativo tentou aplicar um perfil de rede hospedada sem fio a um adaptador de rede sem fio físico usando a função [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) , em vez de um dispositivo virtual.                                                                                                                                                                                                                                                    |
| \_perfil AP de código de motivo de WLAN \_ \_ \_ \_ não \_ permitido              | Um aplicativo tentou aplicar um perfil de rede hospedada sem fio a um adaptador de rede sem fio físico usando a função [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) , em vez de um dispositivo virtual.                                                                                                                                                                                                                                                    |



 

A tabela a seguir lista os códigos de erro de validação de perfil.



| Código de motivo                                                    | Significado                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| código de motivo da WLAN \_ \_ \_ esquema de \_ perfil inválido \_                   | O perfil é inválido de acordo com o esquema.                                                                                                                                                                                                  |
| Perfil de código de motivo de WLAN \_ \_ \_ \_ ausente                           | O elemento WLANProfile está ausente.                                                                                                                                                                                                           |
| código de motivo da WLAN \_ \_ \_ nome do \_ perfil inválido \_                     | O nome do perfil é inválido.                                                                                                                                                                                                           |
| código de motivo da WLAN \_ \_ \_ tipo de \_ perfil inválido \_                     | O tipo do perfil é inválido.                                                                                                                                                                                                           |
| código de motivo da WLAN \_ \_ \_ \_ tipo PHY inválido \_                         | O tipo PHY é inválido.                                                                                                                                                                                                                      |
| código de motivo da WLAN \_ \_ \_ \_ segurança msm \_ ausente                     | As configurações de segurança do MSM estão ausentes.                                                                                                                                                                                                        |
| motivo da WLAN \_ \_ código de segurança de \_ IHV \_ \_ sem \_ suporte              | As configurações de segurança do fornecedor de hardware independente (IHV) estão ausentes.                                                                                                                                                                          |
| código de motivo da WLAN com \_ \_ \_ \_ incompatibilidade de IHV Oui \_                         | O perfil de IHV OUI não correspondeu ao adaptador OUI.                                                                                                                                                                                       |
| código de motivo da WLAN do \_ \_ \_ IHV \_ Oui \_ ausente                          | As configurações do IHV OUI estão ausentes.                                                                                                                                                                                                             |
| código do motivo da WLAN \_ \_ configurações de \_ IHV \_ \_ ausentes                     | As configurações de segurança de IHV estão ausentes.                                                                                                                                                                                                        |
| motivo da WLAN \_ \_ código de conectividade do \_ IHV \_ \_ não \_ suportado          | Um aplicativo tentou aplicar um perfil de IHV em um adaptador que não oferece suporte a configurações de conectividade de IHV.                                                                                                                                   |
| \_segurança de \_ conflito de código de motivo da WLAN \_ \_                         | As configurações de segurança estão em conflito.                                                                                                                                                                                                               |
| segurança do código de motivo da WLAN \_ \_ \_ \_ ausente                          | As configurações de segurança estão ausentes.                                                                                                                                                                                                            |
| código do motivo da WLAN \_ \_ \_ tipo de \_ BSS inválido \_                         | O tipo de BSS não é válido.                                                                                                                                                                                                                    |
| motivo da WLAN \_ \_ código \_ \_ \_ modo de conexão adhoc inválido \_           | A conexão automática não pode ser definida para uma rede ad hoc.                                                                                                                                                                                     |
| \_código de motivo de WLAN \_ \_ sem \_ difusão \_ definida \_ para \_ adhoc            | Não é possível definir não difusão para uma rede ad hoc.                                                                                                                                                                                            |
| \_ \_ \_ \_ conjunto de opções automáticas \_ \_ de código de motivo de WLAN para \_ adhoc              | A opção auto-switch não pode ser definida para uma rede ad hoc.                                                                                                                                                                                              |
| \_ \_ \_ \_ conjunto de opções automáticas \_ de código de motivo WLAN \_ para \_ \_ conexão manual | A opção auto-switch não pode ser definida para um perfil de conexão manual.                                                                                                                                                                                    |
| código de motivo da WLAN com \_ \_ \_ \_ segurança IHV \_ Onex \_ ausente               | As configurações de segurança do IHV 802.1 X estão ausentes.                                                                                                                                                                                                 |
| Perfil de código do motivo da WLAN \_ \_ \_ \_ SSID \_ inválido                     | O SSID no perfil é inválido ou está ausente.                                                                                                                                                                                                |
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
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil de \_ \_ restrição de PreAuth inválido \_         | Restrição de PreAuth inválida.                                                                                                                                                                 |
| código de motivo da WLAN \_ \_ MSMSEC de \_ \_ perfil \_ PreAuth \_ \_ habilitado apenas             | PreAuth habilitado quando o cache PMK está desabilitado.                                                                                                                                               |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ rede de capacidade \_                         | Falha na correspondência de capacidade na rede.                                                                                                                                                    |
| código de motivo da WLAN \_ \_ MSMSEC do \_ \_ recurso \_ NIC                             | Falha na correspondência de capacidade na NIC.                                                                                                                                                        |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil de funcionalidade \_                         | Falha na correspondência de capacidade no perfil.                                                                                                                                                    |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ descoberta de recursos \_                       | A rede não oferece suporte ao tipo de recurso especificado.                                                                                                                                       |
| código de motivo da WLAN \_ \_ MSMSEC do \_ \_ perfil \_ frase secreta \_                   | A frase secreta contém um caractere inválido.                                                                                                                                                    |
| código de motivo da WLAN \_ \_ MSMSEC do \_ \_ perfil \_ keymaterial \_                  | O material da chave contém um caractere inválido.                                                                                                                                                  |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de \_ tipo incorreto \_                     | O tipo de chave especificado não corresponde ao material da chave.                                                                                                                                   |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ \_ célula mista                                 | Suspeita de uma célula mista. O AP não está sinalizando que ele é compatível com um perfil habilitado para privacidade.                                                                                  |
| código de motivo da WLAN \_ \_ MSMSEC do perfil de autenticação de \_ \_ perfis \_ \_ \_ inválido              | O número de temporizadores de autenticação ou o número de tempos limite especificados no perfil é inválido.                                                                                        |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ perfil \_ GKEY inválida \_ \_ INTV                | O intervalo de atualização da chave de grupo especificado no perfil é inválido.                                                                                                                        |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ rede de transição \_                         | Uma "rede de transição" é suspeita. A segurança 802,11 herdada é usada para a próxima tentativa de autenticação.                                                                                  |
| código de motivo da WLAN \_ \_ MSMSEC do \_ \_ perfil chave não \_ \_ mapeada \_ carac                | A chave contém caracteres que não estão no conjunto de caracteres ASCII.                                                                                                                      |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ autenticação de perfil de recurso \_ \_                   | Falha na correspondência de capacidade porque a rede não oferece suporte ao método de autenticação no perfil.                                                                                 |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ codificação do perfil de funcionalidade \_ \_                 | Falha na correspondência de capacidade porque a rede não oferece suporte ao algoritmo de codificação no perfil.                                                                                      |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ modo de segurança do perfil \_ \_                         | O valor do modo FIPS 140-2 no perfil é inválido.                                                                                                                                          |
| código de motivo da WLAN \_ \_ MSMSEC do \_ \_ \_ modo seguro do perfil de funcionalidade \_ \_ \_ NIC        | O perfil requer o modo FIPS 140-2, que não tem suporte da NIC (placa de interface de rede).                                                                                                 |
| código do motivo da WLAN \_ \_ \_ MSMSEC \_ \_ modo seguro do perfil de funcionalidade \_ \_ \_ NW         | O perfil requer o modo FIPS 140-2, que não tem suporte da rede.                                                                                                                      |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de \_ autenticação sem suporte \_                  | O perfil especifica um mecanismo de autenticação sem suporte.                                                                                                                               |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de \_ codificação sem suporte \_                | O perfil especifica uma codificação sem suporte.                                                                                                                                                  |
| \_código de motivo \_ da WLAN \_ MSMSEC \_ \_ falha na solicitação da interface do usuário \_                        | Falha ao enfileirar a solicitação de interface do usuário.                                                                                                                                               |
| código de motivo da WLAN \_ \_ MSMSEC de capacidade da \_ \_ \_ MFP \_ NW \_                    | A LAN sem fio requer a proteção de quadro de gerenciamento (MFP) e a interface de rede não dá suporte à MFP. Para obter mais informações, consulte a emenda IEEE 802.11 w para o padrão 802,11. |



 

A tabela a seguir lista os códigos de erro de conexão MSM.



| Código de motivo                                             | Significado                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ \_ tempo limite de inicialização de autenticação \_        | a autenticação 802.1 x não foi iniciada no tempo configurado.                                                      |
| código do motivo da WLAN \_ \_ \_ MSMSEC \_ \_ tempo limite de êxito da autenticação \_      | a autenticação 802.1 x não foi concluída no tempo configurado.                                                   |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ \_ tempo limite de início da chave \_         | A troca de chaves dinâmicas não foi iniciada no tempo configurado.                                                       |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ \_ tempo limite de êxito da chave \_       | A troca de chaves dinâmicas não foi concluída no tempo configurado.                                                    |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ m3 \_ \_ dados de chave ausente \_      | A mensagem 3 do handshake de 4 vias não tem dados de chave.                                                                    |
| Código de motivo da WLAN \_ \_ \_ MSMSEC \_ m3 \_ ausente do \_ IE             | A mensagem 3 do handshake de 4 vias não tem nenhum IE.                                                                          |
| Código de motivo da WLAN \_ \_ \_ MSMSEC \_ m3 \_ \_ chave do GRP ausente \_       | A mensagem 3 de handshake de 4 vias não tem chave GRP.                                                                     |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ PR \_ IE \_ Matching            | Falha ao corresponder os recursos de segurança do IE em m3.                                                               |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ s \_ IE \_ Matching           | Falha ao corresponder os recursos de segurança do IE secundário em m3.                                                     |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ sem \_ chave emparelhada \_           | Uma chave emparelhada era necessária, mas o ponto de acesso (AP) configurou apenas as chaves de grupo.                                        |
| Código de motivo da WLAN \_ \_ \_ MSMSEC \_ G1 \_ dados de chave ausentes \_ \_      | A mensagem 1 do handshake de chave de grupo não tem dados de chave.                                                                |
| Código de motivo da WLAN \_ \_ \_ MSMSEC \_ G1 \_ \_ chave do GRP ausente \_       | A mensagem 1 do handshake de chave de grupo não tem nenhuma chave de grupo.                                                               |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ ponto \_ indicado \_ inseguro   | Bit de segurança de redefinição de AP após a conexão ser protegida.                                                                |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ sem \_ autenticador           | 802.1 x indicou que não há nenhum autenticador, mas o perfil requer um.                                   |
| código de motivo de WLAN \_ \_ \_ MSMSEC \_ falha de NIC \_                | Falha ao direcionar configurações para NIC.                                                                                 |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ cancelado                   | A operação foi cancelada por um chamador.                                                                              |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ Key \_ Format                 | O formato de chave inserido não está em um formato válido.                                                                     |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ downgrade \_ detectado         | Foi detectado um downgrade de segurança.                                                                               |
| código de motivo da WLAN com \_ \_ \_ suspeita de \_ \_ incompatibilidade de PSK MSMSEC \_    | Suspeita de incompatibilidade de PSK.                                                                                     |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ falha forçada \_             | Houve uma falha forçada porque o método de conexão não era seguro.                                         |
| Código de motivo da WLAN \_ \_ \_ MSMSEC \_ m3 \_ \_ muitos \_ RSNIE        | A mensagem 3 do handshake de 4 vias contém muitos RSN IE (RSN).                                                     |
| Código de motivo de WLAN \_ \_ \_ MSMSEC \_ m2 com dados de \_ chave ausentes \_ \_      | A mensagem 2 do handshake de 4 vias não tem dados de chave (RSN adhoc).                                                        |
| Código de motivo da WLAN \_ \_ \_ MSMSEC \_ m2 \_ ausente do \_ IE             | A mensagem 2 do handshake de 4 vias não tem nenhum IE (RSN adhoc).                                                              |
| código de motivo da WLAN \_ \_ \_ MSMSEC \_ auth \_ WCN \_ concluído        |                                                                                                                  |
| \_ \_ código do motivo \_ da WLAN MSMSEC \_ \_ \_ falha na IU de segurança       | A solicitação de interface do usuário de segurança falhou porque a solicitação não pôde ser enfileirada ou porque o usuário cancelou a solicitação. |
| Código de motivo da WLAN \_ \_ \_ MSMSEC \_ m3 \_ chave do \_ \_ GRP MGMT \_ Key | A mensagem 3 do handshake de 4 vias não tem nenhuma chave de grupo de gerenciamento (RSN).                                                        |
| Código de motivo da WLAN \_ \_ \_ MSMSEC \_ G1 chave de Ger. de \_ \_ Gerenciamento ausente \_ \_ | A mensagem 1 do handshake de chave de grupo não tem nenhuma chave de gerenciamento de grupo.                                                    |



 

A tabela a seguir lista os códigos de motivo do 802.1 X. Os elementos de esquema nomeados abaixo são definidos no esquema OneX e especificados no perfil WLAN.



| Código de motivo                                         | Significado                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| o ONEX \_ não pode \_ identificar o \_ \_ usuário                    | Nenhum usuário está disponível para a autenticação 802.1 X. Esse erro pode ocorrer quando a autenticação do computador está desabilitada e nenhum usuário está conectado ao computador.                              |
| identidade de ONEX \_ \_ não \_ encontrada                          | A identidade 802.1 X não pôde ser encontrada.                                                                                                                                            |
| \_interface do usuário Onex \_ desabilitada                                  | A autenticação só pode ser concluída por meio da interface do usuário e esta interface não pôde ser exibida.                                                                       |
| \_falha de EAP 802.1x \_ \_ recebida                        | Falha na autenticação EAP.                                                                                                                                                     |
| o \_ autenticador Onex \_ não \_ \_ está mais presente            | O autenticador 802.1 X saiu da rede.                                                                                                                               |
| \_ \_ \_ não \_ há suporte para a versão do perfil Onex              | Não há suporte para a versão do perfil OneX fornecido.                                                                                                                         |
| \_ \_ comprimento inválido do perfil Onex \_                      | O perfil OneX tem um comprimento inválido.                                                                                                                                            |
| \_tipo de \_ EAP não permitido de perfil de \_ Onex \_                | O tipo de EAP especificado no perfil OneX (possivelmente fornecido pelo elemento EAPType) não é permitido.                                                                               |
| \_ \_ \_ \_ tipo \_ ou sinalizador de EAP \_ inválido do perfil Onex         | O tipo de EAP especificado no perfil OneX (possivelmente fornecido pelo elemento EAPType) é inválido ou um dos sinalizadores EAP (possivelmente fornecidos no elemento EAPConfig) é inválido. |
| \_ \_ sinalizadores Onex inválidos do perfil Onex \_ \_                 | Os sinalizadores suplicantes (possivelmente fornecidos no elemento EAPConfig) no perfil OneX são inválidos.                                                                                 |
| \_valor de \_ \_ timer inválido do perfil \_ Onex                | Um temporizador especificado no perfil OneX (possivelmente fornecido pelo elemento heldPeriod, authPeriod ou startPeriod) é inválido.                                                        |
| \_ \_ \_ modo suplicante inválido do perfil Onex \_            | O modo suplicante especificado no perfil OneX (possivelmente fornecido pelo elemento suplicante) é inválido.                                                                    |
| \_modo de \_ \_ autenticação inválido do perfil \_ Onex                  | O modo de autenticação especificado no perfil OneX (possivelmente fornecido pelo elemento AuthMode) é inválido.                                                                      |
| \_Propriedades de \_ \_ conexão EAP \_ inválidas do perfil Onex \_ | As propriedades de conexão especificadas no perfil OneX (possivelmente fornecida pelo elemento EAPConfig) são inválidas.                                                                  |



 

## <a name="remarks"></a>Comentários

Um conjunto limitado de códigos de motivo tem suporte no Windows XP com Service Pack 3 (SP3) e na API de LAN sem fio para Windows XP com Service Pack 2 (SP2). Os códigos de erro de validação de perfil com suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2 são os seguintes:

-   código de motivo da WLAN \_ \_ \_ esquema de \_ perfil inválido \_
-   Perfil de código de motivo de WLAN \_ \_ \_ \_ ausente
-   Perfil de código do motivo da WLAN \_ \_ \_ \_ SSID \_ inválido

Os códigos de erro de segurança do MSM com suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2 são os seguintes:

-   código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de \_ \_ chave inválido \_
-   código de motivo da WLAN \_ \_ MSMSEC de \_ \_ chave do perfil \_ \_
-   código de motivo de WLAN \_ \_ MSMSEC do \_ \_ perfil \_ PSK \_ comprimento
-   código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de \_ \_ autenticação inválido \_
-   código de motivo da WLAN \_ \_ MSMSEC do \_ \_ perfil \_ Onex \_ desabilitado
-   código de motivo da WLAN \_ \_ MSMSEC do \_ \_ perfil \_ 802.1x \_ habilitado
-   código de motivo da WLAN \_ \_ \_ MSMSEC \_ rede de capacidade \_
-   código de motivo da WLAN \_ \_ MSMSEC do \_ \_ recurso \_ NIC
-   código de motivo da WLAN \_ \_ MSMSEC do \_ \_ perfil \_ keymaterial \_
-   código de motivo de WLAN \_ \_ \_ MSMSEC \_ perfil de \_ tipo incorreto \_

Os códigos de erro 802.1 x com suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2 são os seguintes:

-   \_ \_ comprimento inválido do perfil Onex \_
-   \_ \_ \_ \_ tipo \_ ou sinalizador de EAP \_ inválido do perfil Onex
-   \_modo de \_ \_ autenticação inválido do perfil \_ Onex
-   \_Propriedades de \_ \_ conexão EAP \_ inválidas do perfil Onex \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/>                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Wlanapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
