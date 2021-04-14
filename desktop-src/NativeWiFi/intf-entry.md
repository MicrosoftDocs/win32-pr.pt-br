---
description: Contém informações detalhadas sobre uma interface exigida por um cliente RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: Estrutura de INTF_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502188"
---
# <a name="intf_entry-structure"></a>\_Estrutura de entrada INTF

\[**INTF \_ A entrada** não tem mais suporte do Windows Vista e do Windows Server 2008. Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante. Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]

Contém informações detalhadas sobre uma interface exigida por um cliente RPC.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**wszGuid**
</dt> <dd>

Um ponteiro para o GUID da interface representado como uma cadeia de caracteres Unicode no seguinte formato: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> <dt>

**wszDescr**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém a descrição da interface que é recuperada pelo serviço de configuração zero sem fio (WZCSVC).

</dd> <dt>

**dwContext**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**ulMediaState**
</dt> <dd>

O estado atual de conexão de mídia NDIS para a interface. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                                  | Significado                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <dt> **Estado da mídia \_ \_ conectado**</dt> <dt>1</dt> </dl>       | A mídia está conectada.<br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <dt>**Mídia \_ ESTADO \_ desconectado**</dt> <dt>0</dt> </dl> | A mídia está desconectada.<br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <dt>**Mídia \_ ESTADO \_ desconhecido**</dt> <dt>-1</dt> </dl>               | O estado da mídia é desconhecido.<br/> |



 

</dd> <dt>

**ulMediaType**
</dt> <dd>

Os tipos de mídia NDIS que a NIC usa atualmente. Quando consultado, o valor desse membro é **NdisMedium802 \_ 3** , conforme definido no arquivo de cabeçalho *Ndispnp. h* .

</dd> <dt>

**ulPhysicalMediaType**
</dt> <dd>

O tipo de mídia NDIS da interface. Quando consultado, o valor desse membro é **NdisPhysicalMediumWirelessLan** conforme definido no arquivo de cabeçalho *Ndispnp. h* .

</dd> <dt>

**nInfraMode**
</dt> <dd>

O modo de infraestrutura atual 802,11 definido na interface.

</dd> <dt>

**nAuthMode**
</dt> <dd>

O modo de autenticação 802,11 atual definido na interface.

A tabela a seguir mostra os valores possíveis para o parâmetro com base na enumeração do **modo de autenticação do NDIS \_ 802 \_ 11 \_ \_** definido no arquivo de cabeçalho *NtDDNdis. h* .



| Valor                                                                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt> </dl>                         | Autenticação de sistema aberto IEEE 802,11.<br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt> </dl>                 | A autenticação compartilhada IEEE 802,11 que usa uma chave de privacidade equivalente com fio (WEP) pré-compartilhada. <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt> </dl> | Modo de comutador automático. Ao usar o modo de comutador automático, a NIC (placa de interface de rede) sem fio tenta o modo de autenticação compartilhado primeiro. Se o modo compartilhado falhar, a NIC tentará usar o modo de autenticação aberta. <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt> </dl>                             | Segurança de WPA (acesso protegido sem fio). A autenticação é executada entre o suplicante, o autenticador e o servidor de autenticação sobre IEEE 802.1 X. As chaves de criptografia são dinâmicas e são derivadas por meio do processo de autenticação. <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt> </dl>                 | Segurança WPA usando uma chave pré-compartilhada. A autenticação é executada entre o suplicante e o autenticador sobre IEEE 802.1 X. As chaves de criptografia são dinâmicas e são derivadas por meio da chave pré-compartilhada usada pelo suplicante e pelo autenticador. <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt> </dl>             | Segurança WPA. A autenticação é executada usando uma chave pré-compartilhada sem autenticação IEEE 802.1 X. As chaves de criptografia são estáticas e são derivadas por meio da chave pré-compartilhada. Esse modo é aplicável somente a tipos de rede ad hoc. <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt> </dl>                         | Segurança WPA2. A autenticação é executada entre o suplicante, o autenticador e o servidor de autenticação sobre IEEE 802.1 X. As chaves de criptografia são dinâmicas e são derivadas por meio do processo de autenticação. <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt> </dl>             | Especifica a segurança WPA2. A autenticação é executada entre o suplicante e o autenticador sobre IEEE 802 1X. As chaves de criptografia são dinâmicas e são derivadas por meio da chave pré-compartilhada usada pelo suplicante e pelo autenticador. <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt> </dl>                             | O valor máximo possível para o valor de enumeração do **\_ modo de autenticação NDIS 802 \_ 11 \_ \_** . Esse não é um valor válido para o modo de autenticação. <br/>                                                                                        |



 

</dd> <dt>

**nWepStatus**
</dt> <dd>

O modo de criptografia 802,11 atual definido na interface.

</dd> <dt>

**dwCtlFlags**
</dt> <dd>

Um valor de bitmask de sinalizadores de controle que indicam como o WZCSVC está operando na interface.

A tabela a seguir mostra os valores de bit possíveis.



| Valor                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <dt>**INTFCTL \_ 0x0007 de \_ máscara cm**</dt> <dt></dt> </dl>      | Um bitmask para o modo de filtro de rede. \_ \_ A máscara INTFCTL cm & dwCtlFlags resultar em um valor da infraestrutura de rede do tipo NDIS \_ 802 \_ 11 \_ \_ . O valor resultante indica se o WZCSVC se conecta somente a redes de infraestrutura, redes Adhoc ou a ambos os tipos de redes.<br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <dt>**INTFCTL \_**</dt> <dt>0x8000</dt> habilitado </dl>       | Indica se WZCSVC deve configurar a interface.<br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <dt>**INTFCTL \_**</dt> <dt>0X4000</dt> de FALLBACK </dl>    | Se uma rede preferencial não estiver disponível, esse valor indicará se o WZCSVC deve configurar automaticamente a NIC para associar a qualquer rede disponível.<br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt> </dl> | Indica se o driver NIC dá suporte a todos os OIDs 802,11 exigidos pelo WZCSVC para funcionar.<br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <dt> **INTFCTL \_ volatile**</dt> <dt>0x1000</dt> </dl> | Indica se os parâmetros de serviço para esta interface devem ser mantidos no registro. <br/> Se esse valor for definido, esses parâmetros serão voláteis e não deverão ser mantidos no registro.<br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <dt> **\_ Política de INTFCTL**</dt> <dt>0x0800</dt> </dl>       | Indica se os parâmetros de serviço para essa interface são enviados por Push por uma política de grupo.<br/> Se esse valor for definido, os parâmetros de serviço serão enviados por push para o computador local pela diretiva de grupo.<br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt> </dl> | Indica se o suporte a 802.1 X está habilitado.<br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

**dwDynFlags**
</dt> <dd>

Um bitmask de sinalizadores dinâmicos que controlam o comportamento dinâmico (não persistente e não-estático) na interface.

Esses bits são úteis para disparar alterações dinâmicas e temporárias no modo como o WZCSVC atua na interface. Nenhum desses bits é mantido no registro, de modo que as configurações não sobreviverão a uma reinicialização do sistema ou a uma sequência de habilitação e ativação do dispositivo.

A tabela a seguir mostra os valores de bit possíveis.



| Valor                                                                                                                                                                                                                            | Significado                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <dt>**INTFDYN \_ NOSCAN**</dt> <dt>0x00000001</dt> </dl> | Indica que o WZCSVC não deve solicitar que a interface execute uma verificação ativa, mas em vez disso, use os valores armazenados em cache no driver NIC.<br/> |



 

</dd> <dt>

**dwCapabilities**
</dt> <dd>

Especifica os recursos do driver.



| Valor                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <dt>**INTFCAP \_ \_ \_ Máscara de codificação máxima**</dt> <dt>0x000000FF</dt> </dl> | Os bits de ordem inferior desse membro são usados para indicar a criptografia máxima com suporte. Os valores possíveis são alguns dos valores de enumeração definidos na estrutura **de \_ \_ \_ \_ status WEP do NDIS 802 11** no arquivo de cabeçalho *NtDDNdis. h* incluído no SDK do Windows.<br/> O \_ valor de 11Encryption1Enabled Ndis802 (2) indica que há suporte para o WEP. Não há suporte para TKIP e AES, e uma chave de transmissão pode ou não estar disponível. <br/> O valor de Ndis802 \_ 11Encryption2Enabled (9) indica que há suporte para TKIP e WEP. Não há suporte para AES e uma chave de transmissão está disponível. <br/> O valor de Ndis802 \_ 11Encryption3Enabled (11) indica que AES, TKIP e WEP têm suporte e uma chave de transmissão está disponível. <br/> O Ndis802 \_ 11EncryptionNotSupported (8) indica que a chave WEP não tem suporte. <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <dt>**INTFCAP \_**</dt> <dt>0x00000100</dt> SSN </dl>                                       | Indica suporte para rede segura simples (SSN), que é um subconjunto do 802.11 i. <br/> O SSN altera a chave de criptografia periodicamente, em oposição ao padrão WEP (Wired Equivaled Privacy), que usa uma chave estática. Para que o SSN funcione, a codificação máxima com suporte deve ser pelo menos TKIP. O SSN foi desenvolvido por um consórcio de fornecedores em 2002 como uma abordagem provisória para melhorar a segurança da LAN sem fio enquanto o padrão IEEE 802.11 i estava sendo concluído.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt> </dl>                              | Indica suporte para o padrão IEEE 802.11 i.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

**rdNicCapabilities**
</dt> <dd>

Um conjunto de recursos para 802.11 i.

A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdNicCapabilities** quando chamado com o sinalizador de **\_ recursos de INTF** passado no parâmetro *dwInflags* . Se a chamada de função for bem-sucedida, o membro **pData** da estrutura de **\_ dados brutos** conterá uma estrutura de **\_ \_ recursos INTF 80211** .

</dd> <dt>

**rdSSID**
</dt> <dd>

Dados binários que contêm o SSID 802,11 atualmente configurado na interface.

A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdSSID** quando chamado com o sinalizador **\_ SSID INTF** passado no parâmetro *dwInflags* . Se a chamada de função for bem-sucedida, o membro **dwDataLen** da estrutura de **\_ dados brutos** conterá o membro **SsidLength** de uma estrutura de **SSID do NDIS \_ 802 \_ 11 \_** e o membro **pData** da estrutura de **\_ dados brutos** conterá o membro **SSID** de uma estrutura de **SSID da NDIS \_ 802 \_ 11 \_** .

A estrutura de **SSID do NDIS \_ 802 \_ 11 \_** é definida no arquivo de cabeçalho *Ntddndis. h* .

</dd> <dt>

**rdBSSID**
</dt> <dd>

Dados binários que contêm o BSSID 802,11 configurado na interface.

A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdBSSID** quando chamado com o sinalizador de **\_ bssid de INTF** passado no parâmetro *dwInflags* . Se a chamada de função for bem-sucedida, o membro **dwDataLen** da estrutura de **\_ dados brutos** conterá o tamanho de uma estrutura de **\_ \_ \_ \_ endereços MAC de NDIS 802 11** e o membro **pData** da estrutura de **\_ dados brutos** conterá a estrutura de **\_ \_ \_ \_ endereço MAC de 802** .

A estrutura de **\_ \_ \_ \_ endereços MAC do NDIS 802 11** é definida no arquivo de cabeçalho *Ntddndis. h* .

</dd> <dt>

**rdBSSIDList**
</dt> <dd>

Dados binários que contêm a lista de BSSIDs que foram recuperados pela última vez por WZCSVC.

A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdBSSIDList** quando chamado com o sinalizador **INTF \_ BSSIDLIST** passado no parâmetro *dwInflags* . Se a chamada de função for bem-sucedida, o membro **dwDataLen** da estrutura de **\_ dados brutos** conterá o comprimento do buffer com os dados retornados e o membro **pData** da estrutura de **\_ dados brutos** conterá a estrutura da **lista de configuração do WZC \_ 802 \_ 11 \_ \_** .

</dd> <dt>

**rdStSSIDList**
</dt> <dd>

Dados binários que contêm a lista de redes preferenciais configuradas para esta interface.

A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdStSSIDList** quando chamado com o sinalizador de **INTF \_ preflist** passado no parâmetro *dwInflags* . Se a chamada de função for bem-sucedida, o membro **dwDataLen** da estrutura de **\_ dados brutos** conterá o comprimento do buffer com os dados retornados e o membro **pData** da estrutura de **\_ dados brutos** conterá a estrutura da **lista de configuração do WZC \_ 802 \_ 11 \_ \_** .

Se uma das redes preferenciais estiver conectada no momento, o membro **dwCtlFlags** da estrutura de **configuração de \_ WLAN \_ do WZC** para a rede terá o conjunto de bits 0x0400 ( **\_ mídia \_ conectada WZCCTL** ).

</dd> <dt>

**rdCtrlData**
</dt> <dd>

Dados binários usados com outros sinalizadores de controle, ao definir parâmetros adicionais na interface.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de **\_ entrada INTF** é usada pelas funções [**WZCQueryInterface**](wzcqueryinterface.md) e [**WZCRefreshInterface**](wzcrefreshinterface.md) .

A estrutura de **\_ dados brutos** é definida da seguinte maneira:


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



O membro *pData* aponta para dados binários. O *dwDataLen* indica o número de bytes apontados por *pData*.

> [!Note]  
> O arquivo de cabeçalho *wzcsapi. h* não está disponível no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP com SP3<br/>                                                       |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 




