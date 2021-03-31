---
title: Chave de file_extension
description: Associa uma extensão de nome de arquivo a um ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823015"
---
# <a name="file_extension-key"></a><span data-ttu-id="113b8-103">Chave de> de <de extensão de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="113b8-103"><file\_extension> Key</span></span>

<span data-ttu-id="113b8-104">Associa uma extensão de nome de arquivo a um ProgID.</span><span class="sxs-lookup"><span data-stu-id="113b8-104">Associates a file name extension with a ProgID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="113b8-105">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="113b8-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a><span data-ttu-id="113b8-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="113b8-106">Remarks</span></span>

<span data-ttu-id="113b8-107">As informações contidas na chave de extensão de nome de arquivo são usadas pelo Windows Explorer e pelos monikers de arquivo.</span><span class="sxs-lookup"><span data-stu-id="113b8-107">The information contained in the file name extension key is used by both the Windows Explorer and file monikers.</span></span> <span data-ttu-id="113b8-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa a chave de extensão de nome de arquivo para fornecer o CLSID associado.</span><span class="sxs-lookup"><span data-stu-id="113b8-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) uses the file name extension key to supply the associated CLSID.</span></span>

<span data-ttu-id="113b8-109">A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.</span><span class="sxs-lookup"><span data-stu-id="113b8-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="113b8-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="113b8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="113b8-111">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="113b8-111">**FileType**</span></span>](filetype-key.md)
</dt> <dt>

[<span data-ttu-id="113b8-112">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="113b8-112">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




