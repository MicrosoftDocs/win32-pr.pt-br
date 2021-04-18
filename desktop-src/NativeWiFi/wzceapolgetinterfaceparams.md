---
description: Obtém parâmetros de configuração EAPOL para a interface LAN sem fio especificada.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Função WZCEapolGetInterfaceParams (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785406"
---
# <a name="wzceapolgetinterfaceparams-function"></a>Função WZCEapolGetInterfaceParams

\[O **WZCEapolGetInterfaceParams** não é mais suportado a partir do Windows Vista e do windows Server 2008. Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante. Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]

A função **WZCEapolGetInterfaceParams** Obtém parâmetros de configuração EAPOL para a interface LAN sem fio especificada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrvAddr* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função. Se esse parâmetro for **nulo**, o serviço de configuração sem fio será chamado no computador local.

Se o parâmetro *pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.

</dd> <dt>

*pwszGuid* \[ no\]
</dt> <dd>

O GUID da interface para a qual os dados serão recuperados.

</dd> <dt>

*dwSizeOfSSID* \[ no\]
</dt> <dd>

O tamanho do identificador de rede para o qual os dados serão recuperados.

</dd> <dt>

*pbSSID* \[ no\]
</dt> <dd>

Um ponteiro para o identificador de rede para o qual os dados serão recuperados.

</dd> <dt>

*pIntfParams* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ parâmetros de INTF de EAPOL**](eapol-intf-params.md) que contém parâmetros de interface.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o \_ êxito do erro se a operação for concluída com êxito; caso contrário, retorna um dos códigos de erro do sistema do Windows.

## <a name="remarks"></a>Comentários

Se o **WZCEapolGetInterfaceParams** retornar o \_ êxito do erro, o chamador deverá chamar [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) para liberar os buffers internos alocados para os dados retornados quando essas informações não forem mais necessárias.

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

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
