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
# <a name="initialize-the-signature-manager"></a><span data-ttu-id="3bbcd-103">Inicializar o Gerenciador de assinatura</span><span class="sxs-lookup"><span data-stu-id="3bbcd-103">Initialize the Signature Manager</span></span>

<span data-ttu-id="3bbcd-104">Este tópico descreve como inicializar o Gerenciador de assinatura para uso com um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="3bbcd-104">This topic describes how to initialize the signature manager for use with an XPS document.</span></span>

<span data-ttu-id="3bbcd-105">Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="3bbcd-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="3bbcd-106">Para usar os recursos do Windows 7 da API de criptografia, defina o símbolo de **informações de OID criptografado \_ \_ \_ com \_ \_ campos adicionais** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3bbcd-106">To use the Windows 7 features of the Crypto API, define the **CRYPT\_OID\_INFO\_HAS\_EXTRA\_FIELDS** symbol as follows:</span></span>


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



<span data-ttu-id="3bbcd-107">Em seguida, crie uma instância de uma interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="3bbcd-107">Next, instantiate an [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), as shown in the following code example.</span></span>


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



<span data-ttu-id="3bbcd-108">A interface instanciada por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pode ser usada por apenas um documento XPS, que deve ser carregado chamando [**loadpackagefile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) ou [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) antes de chamar qualquer outro método.</span><span class="sxs-lookup"><span data-stu-id="3bbcd-108">The interface instantiated by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) can be used by only one XPS document, which must be loaded by calling [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) or [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) before calling any other method.</span></span>

<span data-ttu-id="3bbcd-109">Depois que a interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) tiver sido instanciada e um documento XPS tiver sido carregado, o Gerenciador de assinatura estará pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="3bbcd-109">After the [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bbcd-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bbcd-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3bbcd-111">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="3bbcd-111">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="3bbcd-112">Assinar um documento</span><span class="sxs-lookup"><span data-stu-id="3bbcd-112">Sign a Document</span></span>](sign-a-document.md)
</dt> <dt>

[<span data-ttu-id="3bbcd-113">Adicionar uma solicitação de assinatura a um documento XPS</span><span class="sxs-lookup"><span data-stu-id="3bbcd-113">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="3bbcd-114">Verificar assinaturas de documento</span><span class="sxs-lookup"><span data-stu-id="3bbcd-114">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="3bbcd-115">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="3bbcd-115">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="3bbcd-116">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="3bbcd-116">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="3bbcd-117">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="3bbcd-117">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

<span data-ttu-id="3bbcd-118">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="3bbcd-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="3bbcd-119">Erros de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="3bbcd-119">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="3bbcd-120">Erros de documento XPS</span><span class="sxs-lookup"><span data-stu-id="3bbcd-120">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="3bbcd-121">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="3bbcd-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
