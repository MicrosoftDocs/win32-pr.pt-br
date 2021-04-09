---
description: A propriedade DVDAdm fornece acesso ao objeto MSDVDAdm que contém métodos e propriedades para salvar informações do aplicativo e do usuário.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Propriedade DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087627"
---
# <a name="dvdadm-property"></a><span data-ttu-id="50366-103">Propriedade DVDAdm</span><span class="sxs-lookup"><span data-stu-id="50366-103">DVDAdm Property</span></span>

> [!Note]  
> <span data-ttu-id="50366-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="50366-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="50366-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="50366-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="50366-106">A `DVDAdm` propriedade fornece acesso ao objeto [MSDVDAdm](msdvdadm-object.md) que contém métodos e propriedades para salvar informações do aplicativo e do usuário.</span><span class="sxs-lookup"><span data-stu-id="50366-106">The `DVDAdm` property provides access to the [MSDVDAdm](msdvdadm-object.md) object that contains methods and properties for saving application and user information.</span></span>

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a><span data-ttu-id="50366-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="50366-107">Remarks</span></span>

<span data-ttu-id="50366-108">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="50366-108">This property is read-only with no default value.</span></span> <span data-ttu-id="50366-109">Não é necessário criar uma referência separada para o objeto **MSDVDAdm** .</span><span class="sxs-lookup"><span data-stu-id="50366-109">There is no need to create a separate reference to the **MSDVDAdm** object.</span></span> <span data-ttu-id="50366-110">Para acessar os métodos e as propriedades do objeto, use a `DVDAdm` propriedade, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="50366-110">To access the methods and properties of the object, use the `DVDAdm` property as shown in the following example.</span></span>

## <a name="examples"></a><span data-ttu-id="50366-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="50366-111">Examples</span></span>


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



