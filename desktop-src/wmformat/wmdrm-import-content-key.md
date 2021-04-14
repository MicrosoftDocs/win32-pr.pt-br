---
title: Estrutura de WMDRM_IMPORT_CONTENT_KEY (Drmexternals. h)
description: A estrutura de chave de conteúdo de importação do WMDRM \_ \_ \_ armazena a chave de conteúdo usada na importação de conteúdo protegido.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_IMPORT_CONTENT_KEY
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369282"
---
# <a name="wmdrm_import_content_key-structure"></a><span data-ttu-id="3e0f0-105">\_Estrutura de \_ chave de conteúdo de importação do WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="3e0f0-105">WMDRM\_IMPORT\_CONTENT\_KEY structure</span></span>

<span data-ttu-id="3e0f0-106">A estrutura de chave de conteúdo de importação do WMDRM armazena a chave de conteúdo usada na importação de conteúdo protegido. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-106">The **WMDRM\_IMPORT\_CONTENT\_KEY** structure stores the content key used in importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e0f0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e0f0-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a><span data-ttu-id="3e0f0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3e0f0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e0f0-109">**DW**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="3e0f0-110">Versão.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-110">Version.</span></span>

</dd> <dt>

<span data-ttu-id="3e0f0-111">**cbStructSize**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-111">**cbStructSize**</span></span>
</dt> <dd>

<span data-ttu-id="3e0f0-112">Tamanho da estrutura em bytes.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-112">Size of structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3e0f0-113">**dwIVKeyType**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-113">**dwIVKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="3e0f0-114">Tipo de chave do vetor de inicialização.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-114">Initialization vector key type.</span></span> <span data-ttu-id="3e0f0-115">Defina como WMDRM \_ KeyType \_ RC4.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-115">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="3e0f0-116">**cbIVKey**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-116">**cbIVKey**</span></span>
</dt> <dd>

<span data-ttu-id="3e0f0-117">Tamanho da chave do vetor de inicialização em bytes.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-117">Size of the initialization vector key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3e0f0-118">**dwContentKeyType**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-118">**dwContentKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="3e0f0-119">Tipo de chave de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-119">Content key type.</span></span> <span data-ttu-id="3e0f0-120">Defina para o \_ tipo de KeyType cocktail de WMDRM \_ .</span><span class="sxs-lookup"><span data-stu-id="3e0f0-120">Set to WMDRM\_KEYTYPE\_COCKTAIL.</span></span>

</dd> <dt>

<span data-ttu-id="3e0f0-121">**cbContentKey**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-121">**cbContentKey**</span></span>
</dt> <dd>

<span data-ttu-id="3e0f0-122">Tamanho da chave de conteúdo em bytes.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-122">Size of the content key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3e0f0-123">**rgbKeyData**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-123">**rgbKeyData**</span></span>
</dt> <dd>

<span data-ttu-id="3e0f0-124">Endereço de um buffer que contém a chave de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-124">Address of a buffer containing the content key.</span></span> <span data-ttu-id="3e0f0-125">O tamanho do buffer deve corresponder ao valor de **cbContentKey**.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-125">The buffer size must match the value of **cbContentKey**.</span></span> <span data-ttu-id="3e0f0-126">Essa chave deve corresponder à chave importada da mensagem de licença XMR.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-126">This key should match the key imported from the XMR license message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e0f0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e0f0-127">Remarks</span></span>

<span data-ttu-id="3e0f0-128">Essa estrutura, incluindo o buffer que contém a chave de sessão, deve ser criptografada com a chave de sessão e incluída no membro **pbEncryptedKeyMessage** da estrutura de [**\_ \_ \_ struct init de importação do WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="3e0f0-128">This structure, including the buffer containing the session key, must be encrypted with the session key and included in the **pbEncryptedKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e0f0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e0f0-129">Requirements</span></span>



| <span data-ttu-id="3e0f0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e0f0-130">Requirement</span></span> | <span data-ttu-id="3e0f0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3e0f0-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e0f0-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e0f0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3e0f0-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3e0f0-133">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3e0f0-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e0f0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3e0f0-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e0f0-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3e0f0-136">Versão</span><span class="sxs-lookup"><span data-stu-id="3e0f0-136">Version</span></span><br/>                  | <span data-ttu-id="3e0f0-137">SDK do Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="3e0f0-137">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="3e0f0-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e0f0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e0f0-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e0f0-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e0f0-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e0f0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e0f0-141">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="3e0f0-141">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





