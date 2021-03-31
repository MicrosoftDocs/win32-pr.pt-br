---
title: Chave FileType
description: Usado por GetClassFile para corresponder padrões em vários bytes de arquivo em um arquivo não composto.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Chave do registro de FileType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006084"
---
# <a name="filetype-key"></a><span data-ttu-id="5269b-104">Chave FileType</span><span class="sxs-lookup"><span data-stu-id="5269b-104">FileType Key</span></span>

<span data-ttu-id="5269b-105">Usado por [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para corresponder padrões em vários bytes de arquivo em um arquivo não composto.</span><span class="sxs-lookup"><span data-stu-id="5269b-105">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5269b-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="5269b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span data-ttu-id="5269b-107"><span id="offset"></span><span id="OFFSET"></span>*desvio*</span><span class="sxs-lookup"><span data-stu-id="5269b-107"><span id="offset"></span><span id="OFFSET"></span>*offset*</span></span>
</dt> <dd>

<span data-ttu-id="5269b-108">Determina a distância do início ou do fim do arquivo para iniciar a comparação.</span><span class="sxs-lookup"><span data-stu-id="5269b-108">Determines how far from the beginning or end of the file to begin the comparison.</span></span> <span data-ttu-id="5269b-109">Se o deslocamento for um valor negativo, a comparação começará no final do arquivo menos o valor de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="5269b-109">If the offset is a negative value, the comparison begins from the end of the file minus the offset value.</span></span> <span data-ttu-id="5269b-110">O valor de deslocamento é um tipo decimal, a menos que seja precedido por "0x".</span><span class="sxs-lookup"><span data-stu-id="5269b-110">The offset value is a decimal type unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="5269b-111"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="5269b-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="5269b-112">Representa o comprimento em bytes desde o início até o fim do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5269b-112">Represents the length in bytes from the beginning to the end of the file.</span></span> <span data-ttu-id="5269b-113">Representa o intervalo de bytes no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5269b-113">Represents the byte range in the file.</span></span> <span data-ttu-id="5269b-114">O valor *CB* é um decimal, a menos que seja precedido por "0x".</span><span class="sxs-lookup"><span data-stu-id="5269b-114">The *cb* value is a decimal unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="5269b-115"><span id="mask"></span><span id="MASK"></span>*mascara*</span><span class="sxs-lookup"><span data-stu-id="5269b-115"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="5269b-116">Um valor binário usado para mascaramento, que é executado usando uma operação AND lógica e o intervalo de bytes especificado por *offset* e *CB*.</span><span class="sxs-lookup"><span data-stu-id="5269b-116">A binary value used for masking, which is performed by using a logical AND operation, and the byte range specified by *offset* and *cb*.</span></span> <span data-ttu-id="5269b-117">Se esse valor for omitido, os bytes serão definidos como todos.</span><span class="sxs-lookup"><span data-stu-id="5269b-117">If this value is omitted, the bytes are set to all ones.</span></span> <span data-ttu-id="5269b-118">Esse valor é sempre hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="5269b-118">This value is always hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="5269b-119"><span id="value"></span><span id="VALUE"></span>*valor*</span><span class="sxs-lookup"><span data-stu-id="5269b-119"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="5269b-120">Representa o padrão que deve corresponder a um arquivo para ser desse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5269b-120">Represents the pattern that must match for a file to be of this file type.</span></span> <span data-ttu-id="5269b-121">O padrão é usado para identificar corretamente um formato de arquivo conhecido de seu conteúdo, não por sua extensão.</span><span class="sxs-lookup"><span data-stu-id="5269b-121">The pattern is used to properly identify a known file format from its contents, not by its extension.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5269b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5269b-122">Remarks</span></span>

<span data-ttu-id="5269b-123">As entradas são usadas pela função [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para corresponder padrões em vários bytes de arquivo em um arquivo não composto.</span><span class="sxs-lookup"><span data-stu-id="5269b-123">Entries are used by the [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) function to match patterns against various file bytes in a non-compound file.</span></span> <span data-ttu-id="5269b-124">O **filetype** tem subchaves CLSID, cada uma com uma série de subchaves **0**, **1**, **2**, **3**.</span><span class="sxs-lookup"><span data-stu-id="5269b-124">**FileType** has CLSID subkeys, each of which has a series of subkeys **0**, **1**, **2**, **3**.</span></span> <span data-ttu-id="5269b-125">Esses valores contêm padrões que, se houver correspondência, produzirão o CLSID indicado.</span><span class="sxs-lookup"><span data-stu-id="5269b-125">These values contain patterns that, if one matches, yield the indicated CLSID.</span></span> <span data-ttu-id="5269b-126">Por exemplo, um valor de "0, 4, FFFFFFFF, ABCD1234" indica que os primeiros 4 bytes devem ser ABCD1234, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="5269b-126">For example, a value of "0, 4, FFFFFFFF, ABCD1234" indicates that the first 4 bytes must be ABCD1234, in that order.</span></span> <span data-ttu-id="5269b-127">Um valor de "-4, 4, FEFEFEFE" indica que os últimos quatro bytes no arquivo devem ser FEFEFEFE.</span><span class="sxs-lookup"><span data-stu-id="5269b-127">A value of "-4, 4, FEFEFEFE " indicates that the last four bytes in the file must be FEFEFEFE.</span></span> <span data-ttu-id="5269b-128">Se qualquer um dos padrões corresponder, o CLSID será retornado.</span><span class="sxs-lookup"><span data-stu-id="5269b-128">If either pattern matches, the CLSID is returned.</span></span>

<span data-ttu-id="5269b-129">A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.</span><span class="sxs-lookup"><span data-stu-id="5269b-129">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5269b-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5269b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5269b-131">**><\_ extensão de arquivo**</span><span class="sxs-lookup"><span data-stu-id="5269b-131">**<file\_extension>**</span></span>](-file-extension--key.md)
</dt> <dt>

[<span data-ttu-id="5269b-132">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="5269b-132">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




