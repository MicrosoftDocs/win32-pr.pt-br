---
title: Escolhendo uma interface para associação
description: Quando um objeto de diretório é associado, o chamador especifica o tipo de interface ADSI desejado.
ms.assetid: 3c86e136-6d82-4baf-9c76-27dac8ad68ac
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usando, escolhendo uma interface para associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444bd41d1567849d5bf3a85ac3ec22f317ced5d3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366703"
---
# <a name="choosing-an-interface-for-binding"></a>Escolhendo uma interface para associação

Quando um objeto de diretório é associado, o chamador especifica o tipo de interface ADSI desejado. Todos os objetos de diretório ADSI dão suporte à interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Um objeto ADSI também pode dar suporte a outras interfaces. As interfaces reais com suporte do objeto dependem da classe do objeto. Por exemplo, um objeto de usuário dá suporte à interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) , mas não dará suporte à interface [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) .

Os clientes de automação devem usar as interfaces **IADs \*** porque essas interfaces são de duas interfaces que fornecem um nível maior de abstração e fornecem dados usando o tipo de dados [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .

Além das interfaces **\* IADs** , os clientes C/C++ podem usar as interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Essas interfaces não são interfaces duplas e não oferecem suporte à automação. Essas interfaces oferecem maior controle sobre exatamente quais atributos recuperar e permitir o acesso aos dados brutos armazenados em uma propriedade. Por exemplo, quando o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) é usado para recuperar o **atributo ntSecurityDescriptor** para um objeto, o método **IADs:: Get** fornece um ponteiro de interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que dá suporte à interface [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) . A interface **IADsSecurityDescriptor** é fornecida pela ADSI para representar um descritor de segurança. Em comparação, quando o método [**IDirectoryObject:: Getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) é usado para recuperar o atributo **ntSecurityDescriptor** , **IDirectoryObject:: getobjectattributes** fornece uma matriz de bytes que pode ser convertida em uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . As APIs de segurança do Win32 podem ser usadas com esses dados para manipular o descritor de segurança.

 

 