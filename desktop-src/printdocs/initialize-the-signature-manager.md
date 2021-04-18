---
description: Este tópico descreve como inicializar o Gerenciador de assinatura para uso com um documento XPS.
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: Inicializar o Gerenciador de assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808370"
---
# <a name="initialize-the-signature-manager"></a>Inicializar o Gerenciador de assinatura

Este tópico descreve como inicializar o Gerenciador de assinatura para uso com um documento XPS.

Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md).

Para usar os recursos do Windows 7 da API de criptografia, defina o símbolo de **informações de OID criptografado \_ \_ \_ com \_ \_ campos adicionais** da seguinte maneira:


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



Em seguida, crie uma instância de uma interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), conforme mostrado no exemplo de código a seguir.


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



A interface instanciada por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pode ser usada por apenas um documento XPS, que deve ser carregado chamando [**loadpackagefile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) ou [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) antes de chamar qualquer outro método.

Depois que a interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) tiver sido instanciada e um documento XPS tiver sido carregado, o Gerenciador de assinatura estará pronto para uso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Assinar um documento](sign-a-document.md)
</dt> <dt>

[Adicionar uma solicitação de assinatura a um documento XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Verificar assinaturas de documento](verify-document-signatures.md)
</dt> <dt>

**Usado nesta seção**
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[Erros de API de assinatura digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erros de documento XPS](xps-document-errors.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
