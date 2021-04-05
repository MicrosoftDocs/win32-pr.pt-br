---
title: Estrutura de WMDRM_IMPORT_SESSION_KEY (Drmexternals. h)
description: A estrutura de chave de sessão de importação do WMDRM \_ \_ \_ contém a chave de sessão para importar conteúdo protegido.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_IMPORT_SESSION_KEY
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086097"
---
# <a name="wmdrm_import_session_key-structure"></a><span data-ttu-id="09cab-105">\_Estrutura de \_ chave de sessão de importação WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="09cab-105">WMDRM\_IMPORT\_SESSION\_KEY structure</span></span>

<span data-ttu-id="09cab-106">A estrutura de chave de sessão de importação do WMDRM contém a chave de sessão para importar conteúdo protegido. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="09cab-106">The **WMDRM\_IMPORT\_SESSION\_KEY** structure holds the session key for importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="09cab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09cab-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a><span data-ttu-id="09cab-108">Membros</span><span class="sxs-lookup"><span data-stu-id="09cab-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="09cab-109">**dwKeyType**</span><span class="sxs-lookup"><span data-stu-id="09cab-109">**dwKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="09cab-110">Tipo de chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="09cab-110">Session key type.</span></span> <span data-ttu-id="09cab-111">Defina como WMDRM \_ KeyType \_ RC4.</span><span class="sxs-lookup"><span data-stu-id="09cab-111">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="09cab-112">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="09cab-112">**cbKey**</span></span>
</dt> <dd>

<span data-ttu-id="09cab-113">Tamanho da chave de sessão, em bytes.</span><span class="sxs-lookup"><span data-stu-id="09cab-113">Size of the session key, in bytes.</span></span> <span data-ttu-id="09cab-114">Esse valor pode ser tão grande quanto necessário, considerando os limites de uma única operação RSA OAEP sobre toda a mensagem (essa estrutura e a chave de sessão).</span><span class="sxs-lookup"><span data-stu-id="09cab-114">This value can be as large as you need, given the limits of a single RSA OAEP operation over the entire message (this structure plus the session key).</span></span>

</dd> <dt>

<span data-ttu-id="09cab-115">**rgbKey**</span><span class="sxs-lookup"><span data-stu-id="09cab-115">**rgbKey**</span></span>
</dt> <dd>

<span data-ttu-id="09cab-116">Endereço de um buffer que contém a chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="09cab-116">Address of a buffer containing the session key.</span></span> <span data-ttu-id="09cab-117">O tamanho do buffer deve corresponder ao valor de **cbKey**.</span><span class="sxs-lookup"><span data-stu-id="09cab-117">The buffer size must match the value of **cbKey**.</span></span> <span data-ttu-id="09cab-118">Os dados no buffer são um valor de chave gerado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="09cab-118">The data in the buffer is a randomly generated key value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09cab-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="09cab-119">Remarks</span></span>

<span data-ttu-id="09cab-120">Essa estrutura, incluindo o buffer que contém a chave de sessão, deve ser criptografada com a chave pública do computador DRM do Windows Media e incluída no membro **pbEncryptedSessionKeyMessage** da estrutura de [**\_ \_ \_ struct init Import do WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="09cab-120">This structure, including the buffer containing the session key, must be encrypted with the Windows Media DRM machine public key and included in the **pbEncryptedSessionKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="09cab-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09cab-121">Requirements</span></span>



| <span data-ttu-id="09cab-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="09cab-122">Requirement</span></span> | <span data-ttu-id="09cab-123">Valor</span><span class="sxs-lookup"><span data-stu-id="09cab-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="09cab-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09cab-124">Minimum supported client</span></span><br/> | <span data-ttu-id="09cab-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="09cab-125">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="09cab-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09cab-126">Minimum supported server</span></span><br/> | <span data-ttu-id="09cab-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09cab-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="09cab-128">Versão</span><span class="sxs-lookup"><span data-stu-id="09cab-128">Version</span></span><br/>                  | <span data-ttu-id="09cab-129">SDK do Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="09cab-129">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="09cab-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09cab-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="09cab-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="09cab-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09cab-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="09cab-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09cab-133">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="09cab-133">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





