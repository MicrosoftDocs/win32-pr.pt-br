---
title: DllSurrogate
description: Permite que os servidores DLL sejam executados em um processo substituto. Se uma cadeia de caracteres vazia for especificada, o substituto fornecido pelo sistema será usado; caso contrário, o valor especifica o caminho do substituto a ser usado.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- COM valor do registro DllSurrogate COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366759"
---
# <a name="dllsurrogate"></a><span data-ttu-id="3c234-105">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="3c234-105">DllSurrogate</span></span>

<span data-ttu-id="3c234-106">Permite que os servidores DLL sejam executados em um processo substituto.</span><span class="sxs-lookup"><span data-stu-id="3c234-106">Enables DLL servers to run in a surrogate process.</span></span> <span data-ttu-id="3c234-107">Se uma cadeia de caracteres vazia for especificada, o substituto fornecido pelo sistema será usado; caso contrário, o valor especifica o caminho do substituto a ser usado.</span><span class="sxs-lookup"><span data-stu-id="3c234-107">If an empty string is specified, the system-supplied surrogate is used; otherwise, the value specifies the path of the surrogate to be used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3c234-108">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="3c234-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a><span data-ttu-id="3c234-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c234-109">Remarks</span></span>

<span data-ttu-id="3c234-110">Esse é um valor do **reg \_ sz** que especifica que a classe é uma dll a ser ativada em um processo substituto e o processo substituto a ser usado.</span><span class="sxs-lookup"><span data-stu-id="3c234-110">This is a **REG\_SZ** value that specifies that the class is a DLL that is to be activated in a surrogate process, and the surrogate process to be used.</span></span> <span data-ttu-id="3c234-111">Para usar o processo de substituição genérico fornecido pelo sistema, defina o *caminho* para uma cadeia de caracteres vazia ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3c234-111">To use the system-supplied generic surrogate process, set *path* to an empty string or **NULL**.</span></span> <span data-ttu-id="3c234-112">Para especificar outro processo substituto, defina *caminho* para o caminho do substituto.</span><span class="sxs-lookup"><span data-stu-id="3c234-112">To specify another surrogate process, set *path* to the path of the surrogate.</span></span> <span data-ttu-id="3c234-113">Como na especificação do caminho de um servidor sob a chave [**LocalServer32**](localserver32.md) , uma especificação de caminho completo não é necessária.</span><span class="sxs-lookup"><span data-stu-id="3c234-113">As in the specification of the path of a server under the [**LocalServer32**](localserver32.md) key, a full path specification is not necessary.</span></span> <span data-ttu-id="3c234-114">O substituto deve ser gravado para se comunicar corretamente com o serviço DCOM, conforme descrito em [escrevendo um substituto personalizado](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="3c234-114">The surrogate must be written to properly communicate with the DCOM service as described in [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

<span data-ttu-id="3c234-115">O valor de **DllSurrogate** deve estar presente para que um servidor dll seja ativado em um substituto.</span><span class="sxs-lookup"><span data-stu-id="3c234-115">The **DllSurrogate** value must be present for a DLL server to be activated in a surrogate.</span></span> <span data-ttu-id="3c234-116">A ativação refere-se a uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)ou [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="3c234-116">Activation refers to a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage), or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="3c234-117">A execução de DLLs em um processo substituto fornece os benefícios de uma implementação executável, incluindo o isolamento de falhas, a capacidade de atender a vários clientes simultaneamente e permitir que o servidor forneça serviços a clientes remotos em um ambiente distribuído.</span><span class="sxs-lookup"><span data-stu-id="3c234-117">Running DLLs in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c234-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c234-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c234-119">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="3c234-119">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="3c234-120">Substitutos de DLL</span><span class="sxs-lookup"><span data-stu-id="3c234-120">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="3c234-121">**DllSurrogateExecutable**</span><span class="sxs-lookup"><span data-stu-id="3c234-121">**DllSurrogateExecutable**</span></span>](dllsurrogateexecutable.md)
</dt> <dt>

[<span data-ttu-id="3c234-122">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="3c234-122">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 