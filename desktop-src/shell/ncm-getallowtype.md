---
description: Recupera os tipos de endereço de rede que um controle de endereço de rede especificado aceita.
title: Mensagem de NCM_GETALLOWTYPE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010605"
---
# <a name="ncm_getallowtype-message"></a>\_Mensagem NCM GETallowtype

Recupera os tipos de endereço de rede que um controle de endereço de rede especificado aceita.


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna os tipos de endereço de rede permitidos como uma ou mais constantes de [**\_ cadeia de caracteres net**](net-string.md) .

## <a name="remarks"></a>Comentários

A máscara retornada é o critério usado para validar um endereço de rede na mensagem [**NCM \_ GetAddress**](ncm-getaddress.md) .

Use esta mensagem somente para um controle de endereço de rede. Para criar uma instância, use a classe **msctls \_ netaddress** definida em shellapi. h. Chame [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) em tempo de execução antes de enviar esta mensagem. Isso inicializa a biblioteca de controles comuns que contém o controle de endereço de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NCM \_ SETallowtype**](ncm-setallowtype.md)
</dt> <dt>

[**Getallowtype de NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




