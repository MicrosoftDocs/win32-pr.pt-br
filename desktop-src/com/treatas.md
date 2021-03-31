---
title: Tratados
description: Especifica o CLSID de uma classe que pode emular a classe atual.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Tratar da chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822759"
---
# <a name="treatas"></a><span data-ttu-id="a754d-104">Tratados</span><span class="sxs-lookup"><span data-stu-id="a754d-104">TreatAs</span></span>

<span data-ttu-id="a754d-105">Especifica o CLSID de uma classe que pode emular a classe atual.</span><span class="sxs-lookup"><span data-stu-id="a754d-105">Specifies the CLSID of a class that can emulate the current class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a754d-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="a754d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a><span data-ttu-id="a754d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a754d-107">Remarks</span></span>

<span data-ttu-id="a754d-108">Este é um valor de **\_ sz do reg** .</span><span class="sxs-lookup"><span data-stu-id="a754d-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="a754d-109">A emulação é a capacidade de um aplicativo abrir e editar um objeto de uma classe diferente, mantendo o formato original do objeto.</span><span class="sxs-lookup"><span data-stu-id="a754d-109">Emulation is the ability of one application to open and edit an object of a different class, while retaining the original format of the object.</span></span> <span data-ttu-id="a754d-110">A resolução ocorre no computador local, portanto, no caso de ativação remota, a resolução ocorre no computador cliente usando o CLSID especificado por **tratados**.</span><span class="sxs-lookup"><span data-stu-id="a754d-110">Resolution occurs on the local computer, so in remote activation case, resolution occurs on the client computer using the CLSID specified by **TreatAs**.</span></span>

<span data-ttu-id="a754d-111">O DCOM examina o registro local de **tratados**, mesmo se você chamar a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e especificar um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="a754d-111">DCOM looks at the local registry for **TreatAs**, even if you call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function and specify a remote server.</span></span> <span data-ttu-id="a754d-112">Isso significa que, se você tiver uma entrada **Treats** para Class1 a ser tratada como class2 em seu computador local, mas você chamar **CoCreateInstance** para criar uma instância de Class1 e especificar um servidor remoto, o DCOM tentará criar uma instância de class2 no servidor remoto, mesmo se o class2 não estiver registrado no servidor remoto, o que fará com que a chamada de **CoCreateInstance** falhe.</span><span class="sxs-lookup"><span data-stu-id="a754d-112">This means that if you have a **TreatAs** entry for Class1 to be treated as Class2 on your local computer, but you call **CoCreateInstance** to create an instance of Class1 and you specify a remote server, DCOM will try to create an instance of Class2 on the remote server, even if Class2 is not registered on the remote server, which will cause the call to **CoCreateInstance** to fail.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a754d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a754d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a754d-114">**Tratados autotratações**</span><span class="sxs-lookup"><span data-stu-id="a754d-114">**AutoTreatAs**</span></span>](autotreatas.md)
</dt> <dt>

[<span data-ttu-id="a754d-115">**CoGetTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="a754d-115">**CoGetTreatAsClass**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[<span data-ttu-id="a754d-116">**CoTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="a754d-116">**CoTreatAsClass**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




