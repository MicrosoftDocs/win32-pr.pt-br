---
title: Conversão
description: Usado pela caixa de diálogo Converter para determinar os formatos que um aplicativo pode ler e gravar.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Conversão da chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498805"
---
# <a name="conversion"></a><span data-ttu-id="75f4c-104">Conversão</span><span class="sxs-lookup"><span data-stu-id="75f4c-104">Conversion</span></span>

<span data-ttu-id="75f4c-105">Usado pela caixa de diálogo **converter** para determinar os formatos que um aplicativo pode ler e gravar.</span><span class="sxs-lookup"><span data-stu-id="75f4c-105">Used by the **Convert** dialog box to determine the formats an application can read and write.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="75f4c-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="75f4c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a><span data-ttu-id="75f4c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="75f4c-107">Remarks</span></span>

<span data-ttu-id="75f4c-108">As informações de conversão são usadas pela caixa de diálogo **converter** para determinar quais formatos um aplicativo pode ler e gravar.</span><span class="sxs-lookup"><span data-stu-id="75f4c-108">Conversion information is used by the **Convert** dialog box to determine what formats an application can read and write.</span></span> <span data-ttu-id="75f4c-109">Um formato de arquivo delimitado por vírgula é indicado por um número, se for um dos formatos de área de transferência definidos em Windows. h.</span><span class="sxs-lookup"><span data-stu-id="75f4c-109">A comma-delimited file format is indicated by a number if it is one of the Clipboard formats defined in Windows.h.</span></span> <span data-ttu-id="75f4c-110">Uma cadeia de caracteres indica que o formato não é um definido no Windows. h (privado).</span><span class="sxs-lookup"><span data-stu-id="75f4c-110">A string indicates the format is not one defined in Windows.h (private).</span></span> <span data-ttu-id="75f4c-111">Nesse caso, o formato legível e gravável é a \_ estrutura de tópicos do CF (privado).</span><span class="sxs-lookup"><span data-stu-id="75f4c-111">In this case, the readable and writable format is CF\_OUTLINE (private).</span></span>

<span data-ttu-id="75f4c-112">O valor *rformat* especifica o formato de arquivo que um aplicativo pode ler (converter de).</span><span class="sxs-lookup"><span data-stu-id="75f4c-112">The *rformat* value specifies the file format an application can read (convert from).</span></span>

<span data-ttu-id="75f4c-113">O valor *rwformat* especifica o formato de arquivo que um aplicativo pode ler e gravar (ativar como).</span><span class="sxs-lookup"><span data-stu-id="75f4c-113">The *rwformat* value specifies the file format an application can read and write (activate as).</span></span>

 

 




