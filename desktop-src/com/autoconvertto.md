---
title: Converter autoconverteto
description: Especifica a conversão automática de uma determinada classe de objetos em uma nova classe de objetos.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Conversão de chave de registro COM autoconverterto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822152"
---
# <a name="autoconvertto"></a><span data-ttu-id="5a226-104">Converter autoconverteto</span><span class="sxs-lookup"><span data-stu-id="5a226-104">AutoConvertTo</span></span>

<span data-ttu-id="5a226-105">Especifica a conversão automática de uma determinada classe de objetos em uma nova classe de objetos.</span><span class="sxs-lookup"><span data-stu-id="5a226-105">Specifies the automatic conversion of a given class of objects to a new class of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5a226-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="5a226-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a><span data-ttu-id="5a226-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a226-107">Remarks</span></span>

<span data-ttu-id="5a226-108">Este é um valor de **\_ sz de reg** que especifica o identificador de classe do objeto para o qual o objeto ou a classe de objetos fornecida deve ser convertida.</span><span class="sxs-lookup"><span data-stu-id="5a226-108">This is a **REG\_SZ** value that specifies the class identifier of the object to which the given object or class of objects should be converted.</span></span>

<span data-ttu-id="5a226-109">Normalmente, essa chave é usada para converter automaticamente os arquivos criados por uma versão mais antiga de um aplicativo em uma versão mais recente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5a226-109">This key is typically used to automatically convert files created by an older version of an application to a newer version of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a226-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a226-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a226-111">**OleDoAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="5a226-111">**OleDoAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[<span data-ttu-id="5a226-112">**OleGetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="5a226-112">**OleGetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[<span data-ttu-id="5a226-113">**OleSetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="5a226-113">**OleSetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




