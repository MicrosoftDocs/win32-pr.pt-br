---
title: Interface INapComponentInfo (NapCommon.h)
description: Fornece métodos que os componentes de plug-in (como SHAs e SHVs) devem implementar para que o sistema NAP se comunique com eles.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- INapComponentInfo interface NAP
- NAP da interface INapComponentInfo, descrita
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188aae04ab407c5ae26e1d1a764e9093cc101cbe7d714ef8a8e0146013fefee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799701"
---
# <a name="inapcomponentinfo-interface"></a>Interface INapComponentInfo

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A interface **INapComponentInfo** fornece métodos que os componentes de plug-in (como SHAs e SHVs) devem implementar para que o sistema NAP se comunique com eles. O sistema NAP chama sua implementação desses métodos para recuperar informações administrativas estáticas (por exemplo, nome amigável ou cadeias de caracteres localizadas).

## <a name="members"></a>Membros

A interface **INapComponentInfo** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapComponentInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapComponentInfo** tem esses métodos.



| Método                                                                                                         | Descrição                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Usado pelo sistema NAP para solicitar que o cliente de saúde converta um código de erro HRESULT em uma ID de mensagem.<br/> |
| [**INapComponentInfo::GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Usado pelo sistema NAP para obter a descrição de um cliente de saúde.<br/>                                  |
| [**INapComponentInfo::GetFriendlyName**](inapcomponentinfo-getfriendlyname-method.md)                         | Usado pelo sistema NAP para obter o nome amigável de um cliente de saúde.<br/>                                |
| [**INapComponentInfo::GetIcon**](inapcomponentinfo-geticon-method.md)                                         | Usado pelo sistema NAP para obter o ícone de um cliente de saúde.<br/>                                         |
| [**INapComponentInfo::GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | Usado pelo sistema NAP para obter cadeias de caracteres localizadas.<br/>                                                   |
| [**INapComponentInfo::GetVendorName**](inapcomponentinfo-getvendorname-method.md)                             | Usado pelo sistema NAP para obter o nome do fornecedor de um cliente de saúde.<br/>                                  |
| [**INapComponentInfo::GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Usado pelo sistema NAP para obter a versão de um cliente de saúde.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referência nap](nap-reference.md)
</dt> </dl>

 

