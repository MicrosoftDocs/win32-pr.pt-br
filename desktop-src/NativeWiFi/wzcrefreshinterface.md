---
description: Atualiza informações de interface para uma interface LAN sem fio específica.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Função WZCRefreshInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297271"
---
# <a name="wzcrefreshinterface-function"></a>Função WZCRefreshInterface

\[Não há suporte para **WZCRefreshInterface** a partir do Windows Vista e do windows Server 2008. Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante. Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]

A função **WZCRefreshInterface** atualiza informações de interface para uma interface LAN sem fio específica.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrvAddr* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função. Se esse parâmetro for **nulo**, o serviço de configuração sem fio será chamado no computador local.

Se o parâmetro *pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.

</dd> <dt>

*dwInFlags* \[ no\]
</dt> <dd>

Um conjunto de campos a ser atualizado junto com as ações de atualização específicas a serem executadas. Esse é um bitmask que pode conter qualquer combinação dos sinalizadores a seguir.



| Valor                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_**</dt> <dt>0X00010000</dt> de descr </dl>             | Atualize a descrição da interface para uma interface de LAN sem fio.<br/> A descrição da interface atualizada pode ser recuperada chamando-se a função [**WZCQueryInterface**](wzcqueryinterface.md) com o bit **\_ descr INTF** definido no parâmetro *dwInFlags* . A descrição da interface é retornada no membro **wszDescr** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *PIntf* que é retornado pela função **WZCQueryInterface** .<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl> | Atualize as informações de mídia do NDIS para uma interface de LAN sem fio.<br/> As informações de mídia NDIS atualizadas podem ser recuperadas chamando a função [**WZCQueryInterface**](wzcqueryinterface.md) com o bit **INTF \_ NDISMEDIA** definido no parâmetro *dwInFlags* . As informações de mídia do NDIS são retornadas nos membros **ulMediaState**, **ulMediaType** e **UlPhysicalMediaType** da estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* que é retornado pela função **WZCQueryInterface** .<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**INTF \_ Todos os \_ OIDs**</dt> <dt>0xFFF00000</dt> </dl>   | Atualize todos os OIDs de NDIS para uma interface de LAN sem fio. Esta opção atualiza a maioria dos dados para uma interface de LAN sem fio.<br/> As informações atualizadas podem ser recuperadas chamando a função [**WZCQueryInterface**](wzcqueryinterface.md) .<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pIntf* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ entrada INTF**](intf-entry.md) que contém a chave da interface a ser atualizada.

</dd> <dt>

*pdwOutFlags* \[ fora\]
</dt> <dd>

Um conjunto de campos que foram atualizados com êxito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Arena de erro em \_ \_ Trash**</dt> </dl>     | Os blocos de controle de armazenamento foram destruídos. Esse erro será retornado se o serviço de configuração zero sem fio não tiver inicializado objetos internos.<br/>                                                                                                                      |
| <dl> <dt>**arquivo de erro \_ \_ não \_ encontrado**</dt> </dl>   | O sistema não pode encontrar o arquivo especificado. Esse erro será retornado se o GUID no membro **wszGuid** da estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* não coincidir com nenhuma das interfaces de LAN sem fio no computador local. <br/> |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl> | Um parâmetro está incorreto. Esse erro será retornado se o parâmetro *pIntf* for **nulo**. Esse erro será retornado se o membro **wszGuid** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* for **nulo**. <br/>                            |
| <dl> <dt>**STATUS do RPC \_**</dt> </dl>               | Vários códigos de erro.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

O membro **wszGuid** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* deve conter um GUID de interface para uma interface de LAN sem fio. Uma lista de interfaces de LAN sem fio pode ser recuperada chamando a função [**WZCEnumInterfaces**](wzcenuminterfaces.md) .

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

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**\_entrada INTF**](intf-entry.md)
</dt> </dl>

 

 




