---
description: Fornece informações detalhadas para uma interface de LAN sem fio gerenciada pelo serviço de Configuração Sem Fio Zero.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Função WZCQueryInterface (Wzcsapi.h)
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
ms.openlocfilehash: 3dd7ce876501486b9bec4dbad63ce5812b910b32b9dcdaa1eb80aff3e7cc415e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797406"
---
# <a name="wzcqueryinterface-function"></a>Função WZCQueryInterface

\[**O WZCQueryInterface** não tem mais suporte a partir do Windows Vista e Windows Server 2008. Em vez disso, [**use a função WlanQueryInterface.**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) Para obter mais informações, consulte [Sobre a API Wifi nativa.](about-the-native-wifi-api.md) \]

A **função WZCQueryInterface** fornece informações detalhadas para uma interface de LAN sem fio gerenciada pelo serviço de Configuração Sem Fio Zero.

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

*pSrvAddr* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função. Se esse parâmetro for **NULL,** o serviço de Configuração Sem Fio Zero será consultado no computador local.

Se o *parâmetro pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.

</dd> <dt>

*dwInFlags* \[ Em\]
</dt> <dd>

Os campos a serem consultados. Esse é um bitmask que pode conter qualquer combinação dos sinalizadores a seguir.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_ DYNFLAGS**</dt> <dt>0x00000010</dt> </dl>             | Retornar o valor do **membro dwDynFlags** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ DESCR**</dt> <dt>0x00010000</dt> </dl>                      | Retornar o valor do **membro wszDescr** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl>          | Retorne os valores para os membros **ulMediaState**, **ulMediaType** e **ulPhysicalMediaType** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_ PREFLIST**</dt> <dt>0x00040000</dt> </dl>             | Retornar a lista preferencial de redes no **membro rdStSSIDList** da estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_ RECURSOS**</dt> <dt>0X00080000</dt> </dl> | Retorne os valores para **os membros dwCapabilities** e **rdNicCapabilities** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_ INFRAMODE**</dt> <dt>0x00200000</dt> </dl>          | Retornar o valor para o **membro nInfraMode** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/> O **membro nInfraMode** é válido somente em alguns estados de contexto de interface.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_ AUTHMODE**</dt> <dt>0x00400000</dt> </dl>             | Retornar o valor do **membro nAuthMode** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.* <br/> O **membro nAuthMode** é válido somente em alguns estados de contexto de interface.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_ WEPSTATUS**</dt> <dt>0x00800000</dt> </dl>          | Retornar o valor do **membro nWepStatus** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.* <br/> O **membro nWepStatus** é válido somente em alguns estados de contexto de interface.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt> </dl>                         | Retornar o valor do **membro rdSSID** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/> O **membro rdSSID** é válido somente em alguns estados de contexto de interface.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt> </dl>                      | Retornar o valor do **membro rdBSSID** na estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/> O **membro rdBSSID** é válido somente em alguns estados de contexto de interface.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_ BSSIDLIST**</dt> <dt>0x04000000</dt> </dl>          | Retornar a lista visível de redes no **membro rdBSSIDList** da estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo *parâmetro pIntf.*<br/> O **membro rdBSSIDList** é válido somente em alguns estados de contexto de interface.<br/> |



 

</dd> <dt>

*pIntf* \[ in, out\]
</dt> <dd>

Na entrada, um ponteiro para a chave da interface a ser consultada. Na saída, um ponteiro para os dados de interface solicitados. Esse parâmetro é um ponteiro para uma [**estrutura INTF \_ ENTRY.**](intf-entry.md)

</dd> <dt>

*pdwOutFlags* \[ out\]
</dt> <dd>

Um conjunto de campos recuperados com êxito.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.



| Código de retorno                                                                                               | Descrição                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRO \_ QUE NÃO FOI \_ LANÇADO**</dt> </dl>      | Os blocos de controle de armazenamento foram destruídos. Esse erro será retornado se o serviço de Configuração Sem Fio Zero não tiver inicializado objetos internos.<br/>                                                                                                                      |
| <dl> <dt>**ARQUIVO \_ DE ERRO NÃO \_ \_ ENCONTRADO**</dt> </dl>    | O sistema não pode encontrar o arquivo especificado. Esse erro será retornado se o GUID no **membro wszGuid** da estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo parâmetro *pIntf* não corresponder a nenhuma das interfaces de LAN sem fio no computador local. <br/> |
| <dl> <dt>**ERRO \_ PARÂMETRO \_ INVÁLIDO**</dt> </dl>  | Um parâmetro está incorreto. Esse erro será retornado se o *parâmetro pIntf* for **NULL.** Esse erro será retornado se o **membro wszGuid** da estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo parâmetro *pIntf* for **NULL.** <br/>                            |
| <dl> <dt>**ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**</dt> </dl> | Não há memória suficiente disponível para processar essa solicitação e alocar memória para os resultados da consulta.<br/>                                                                                                                                                                       |
| <dl> <dt>**STATUS DE RPC \_**</dt> </dl>                | Vários códigos de erro.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

O **membro wszGuid** da estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo parâmetro *pIntf* deve conter um GUID de interface para uma interface LAN sem fio. Uma lista de interfaces LAN sem fio pode ser recuperada chamando a [**função WZCEnumInterfaces.**](wzcenuminterfaces.md)

Os seguintes membros da estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada por *pIntf* devem ser definidos como 0 antes de uma chamada para a função **WZCQueryInterface:** **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** e **rdCtrlData**.

O serviço de Configuração Sem Fio Zero não atualiza automaticamente o estado da mídia, mesmo quando os eventos conectados e desconectados de mídia são recebidos. Um aplicativo deve forçar uma atualização de estado de mídia chamando a função [**WZCRefreshInterface**](wzcrefreshinterface.md) antes de chamar a função **WZCQueryInterface** se o estado de mídia NDIS for solicitado (o bit NDISMEDIA do INTF será definido no parâmetro \_ *dwInFlags).*

Quando o parâmetro *dwInFlags* contém **INTF \_ BSSIDLIST**, a função **WZCQueryInterface** não definirá *dwOutFlags* com **INTF \_ BSSIDLIST** se a lista visível de redes estiver vazia. Quando o parâmetro *dwInFlags* contém **INTF \_ SSID,** a função **WZCQueryInterface** não definirá *o dwOutFlags* com **\_ INTF SSID** se nenhum SSID estiver disponível.

Se a **função WZCQueryInterface** retornar ERROR SUCCESS, o chamador deverá chamar a função LocalFree com o parâmetro \_ *pIntf* para liberar os buffers internos alocados para os dados retornados depois que essas informações não são mais necessárias. [](/windows/win32/api/winbase/nf-winbase-localfree) Isso libera os buffers usados pelos membros **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** e **rdCtrlData** da estrutura [**INTF \_ ENTRY**](intf-entry.md) apontada pelo parâmetro *pIntf.*

> [!Note]  
> O *arquivo de título Wzcsapi.h* e o arquivo de biblioteca de importação *Wzcsapi.lib* não estão disponíveis no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| Fim do suporte ao cliente<br/>    | Windows XP com SP3<br/>                                                         |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wzcsapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ENTRADA \_ INTF**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
