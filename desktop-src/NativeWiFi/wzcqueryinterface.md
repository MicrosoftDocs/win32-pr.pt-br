---
description: Fornece informações detalhadas para uma interface de LAN sem fio gerenciada pelo serviço de configuração zero sem fio.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Função WZCQueryInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829781"
---
# <a name="wzcqueryinterface-function"></a>Função WZCQueryInterface

\[O **WZCQueryInterface** não é mais suportado a partir do Windows Vista e do windows Server 2008. Em vez disso, use a função [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) . Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md). \]

A função **WZCQueryInterface** fornece informações detalhadas para uma interface de LAN sem fio gerenciada pelo serviço de configuração zero sem fio.

Fornece informações detalhadas para uma determinada interface.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrvAddr* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função. Se esse parâmetro for **nulo**, o serviço de configuração sem fio não será consultado no computador local.

Se o parâmetro *pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.

</dd> <dt>

*dwInFlags* \[ no\]
</dt> <dd>

Os campos a serem consultados. Esse é um bitmask que pode conter qualquer combinação dos sinalizadores a seguir.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_ DYNFLAGS**</dt> <dt>0x00000010</dt> </dl>             | Retorne o valor para o membro **dwDynFlags** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_**</dt> <dt>0X00010000</dt> de descr </dl>                      | Retorne o valor para o membro **wszDescr** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl>          | Retorne os valores para os membros **ulMediaState**, **ulMediaType** e **UlPhysicalMediaType** na estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_ PREFlist**</dt> <dt>0x00040000</dt> </dl>             | Retorne a lista preferencial de redes no membro **rdStSSIDList** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_ RECURSOS**</dt> <dt>0x00080000</dt> </dl> | Retorne os valores para **dwCapabilities** e os membros **rdNicCapabilities** na estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_**</dt> <dt>0X00200000</dt> de infravermelho </dl>          | Retorne o valor para o membro **nInfraMode** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/> O membro **nInfraMode** é válido somente em alguns Estados de contexto de interface.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_ 0x00400000 AUTHmode**</dt> <dt></dt> </dl>             | Retorne o valor para o membro **nAuthMode** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* . <br/> O membro **nAuthMode** é válido somente em alguns Estados de contexto de interface.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_ WEPSTATUS**</dt> <dt>0x00800000</dt> </dl>          | Retorne o valor para o membro **nWepStatus** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* . <br/> O membro **nWepStatus** é válido somente em alguns Estados de contexto de interface.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_**</dt> <dt>0x01000000</dt> SSID </dl>                         | Retorne o valor para o membro **rdSSID** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/> O membro **rdSSID** é válido somente em alguns Estados de contexto de interface.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt> </dl>                      | Retorne o valor para o membro **rdBSSID** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/> O membro **rdBSSID** é válido somente em alguns Estados de contexto de interface.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_ BSSIDLIST**</dt> <dt>0x04000000</dt> </dl>          | Retorne a lista visível de redes no membro **rdBSSIDList** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .<br/> O membro **rdBSSIDList** é válido somente em alguns Estados de contexto de interface.<br/> |



 

</dd> <dt>

*pIntf* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para a chave da interface a ser consultada. Na saída, um ponteiro para os dados de interface solicitados. Esse parâmetro é um ponteiro para uma estrutura de [**\_ entrada INTF**](intf-entry.md) .

</dd> <dt>

*pdwOutFlags* \[ fora\]
</dt> <dd>

Um conjunto de campos recuperados com êxito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.



| Código de retorno                                                                                               | Descrição                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Arena de erro em \_ \_ Trash**</dt> </dl>      | Os blocos de controle de armazenamento foram destruídos. Esse erro será retornado se o serviço de configuração zero sem fio não tiver inicializado objetos internos.<br/>                                                                                                                      |
| <dl> <dt>**arquivo de erro \_ \_ não \_ encontrado**</dt> </dl>    | O sistema não pode encontrar o arquivo especificado. Esse erro será retornado se o GUID no membro **wszGuid** da estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* não coincidir com nenhuma das interfaces de LAN sem fio no computador local. <br/> |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>  | Um parâmetro está incorreto. Esse erro será retornado se o parâmetro *pIntf* for **nulo**. Esse erro será retornado se o membro **wszGuid** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* for **nulo**. <br/>                            |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl> | Não há memória suficiente disponível para processar essa solicitação e alocar memória para os resultados da consulta.<br/>                                                                                                                                                                       |
| <dl> <dt>**STATUS do RPC \_**</dt> </dl>                | Vários códigos de erro.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

O membro **wszGuid** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* deve conter um GUID de interface para uma interface de LAN sem fio. Uma lista de interfaces de LAN sem fio pode ser recuperada chamando a função [**WZCEnumInterfaces**](wzcenuminterfaces.md) .

Os seguintes membros da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada por *pIntf* devem ser definidos como 0 antes de uma chamada para a função **WZCQueryInterface** : **RdSSID**, **rdBSSID** **, rdBSSIDList,** **rdStSSIDList** e **rdCtrlData**.

O serviço de configuração zero sem fio não automotically atualizar o estado da mídia, mesmo quando a mídia conectada e os eventos desconectados são recebidos. Um aplicativo deve forçar uma atualização de estado de mídia chamando a função [**WZCRefreshInterface**](wzcrefreshinterface.md) antes de chamar a função **WZCQueryInterface** se o estado de mídia NDIS for solicitado (o \_ bit INTF NDISMEDIA será definido no parâmetro *dwInFlags* ).

Quando o parâmetro *dwInFlags* contiver **INTF \_ BSSIDLIST**, a função **WZCQueryInterface** não definirá *dwOutFlags* com **INTF \_** BSSIDLIST se a lista de redes visível estiver vazia. Quando o parâmetro *dwInFlags* contiver **INTF \_ SSID**, a função **WZCQueryInterface** não definirá o *dwOutFlags* com **INTF \_ SSID** se nenhum SSID estiver disponível.

Se a função **WZCQueryInterface** retornar o \_ êxito do erro, o chamador deverá chamar a função [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) com o parâmetro *pIntf* para liberar os buffers internos alocados para os dados retornados quando essas informações não forem mais necessárias. Isso libera os buffers usados pelos membros **rdSSID**, **rdBSSID**, **rdBSSIDList**, **RdStSSIDList** e **RdCtrlData** da estrutura de [**\_ entrada INTF**](intf-entry.md) apontada por *pIntf* parâmetro.

> [!Note]  
> O arquivo de cabeçalho *wzcsapi. h* e o arquivo de biblioteca de importação *wzcsapi. lib* não estão disponíveis no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows XP com SP3<br/>                                                         |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_entrada INTF**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
