---
title: Interface INapComponentInfo (NapCommon. h)
description: Fornece métodos que os componentes de plug-in (como SHAs e SHVs) devem implementar para que o sistema NAP se comunique com eles.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- INapComponentInfo da interface NAP
- INapComponentInfo interface NAP, descrita
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
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918241"
---
# <a name="inapcomponentinfo-interface"></a>Interface INapComponentInfo

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapComponentInfo** fornece métodos que os componentes de plug-in (como Shas e SHVs) devem implementar para que o sistema NAP se comunique com eles. O sistema NAP chama a implementação desses métodos para recuperar informações administrativas estáticas (por exemplo, nome amigável ou cadeias de caracteres localizadas).

## <a name="members"></a>Membros

A interface **INapComponentInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapComponentInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapComponentInfo** tem esses métodos.



| Método                                                                                                         | Descrição                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Usado pelo sistema NAP para solicitar que o cliente de integridade Converta um código de erro HRESULT em uma ID de mensagem.<br/> |
| [**INapComponentInfo:: GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Usado pelo sistema NAP para obter a descrição de um cliente de integridade.<br/>                                  |
| [**INapComponentInfo:: getfriendlyname**](inapcomponentinfo-getfriendlyname-method.md)                         | Usado pelo sistema NAP para obter o nome amigável de um cliente de integridade.<br/>                                |
| [**INapComponentInfo:: GetIcon**](inapcomponentinfo-geticon-method.md)                                         | Usado pelo sistema NAP para obter o ícone de um cliente de integridade.<br/>                                         |
| [**INapComponentInfo:: gettraduzistring**](inapcomponentinfo-getlocalizedstring-method.md)                   | Usado pelo sistema NAP para obter cadeias de caracteres localizadas.<br/>                                                   |
| [**INapComponentInfo:: getvendoname**](inapcomponentinfo-getvendorname-method.md)                             | Usado pelo sistema NAP para obter o nome do fornecedor de um cliente de integridade.<br/>                                  |
| [**INapComponentInfo:: GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Usado pelo sistema NAP para obter a versão de um cliente de integridade.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

