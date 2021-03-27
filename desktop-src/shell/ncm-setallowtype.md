---
description: Define os tipos de endereço de rede que um controle de endereço de rede especificado aceita.
title: Mensagem de NCM_SETALLOWTYPE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647538"
---
# <a name="ncm_setallowtype-message"></a>\_Mensagem NCM SETallowtype

Define os tipos de endereço de rede que um controle de endereço de rede especificado aceita.


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*addrMask* \[ no\]
</dt> <dd>Especifica os tipos de endereço de rede como uma ou mais constantes de <a href="net-string.md">**\_ cadeia de caracteres net**</a> .</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido, ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

O conjunto de máscaras é o critério usado para validar um endereço de rede na mensagem [**NCM \_ GetAddress**](ncm-getaddress.md) .

Use esta mensagem somente para um controle de endereço de rede. Para criar uma instância, use a classe **msctls \_ netaddress** definida em shellapi. h. Chame [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) em tempo de execução antes de enviar esta mensagem. Isso inicializa a biblioteca de controles comuns que contém o controle de endereço de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NCM \_ GETallowtype**](ncm-getallowtype.md)
</dt> <dt>

[**SetAllowType de NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




