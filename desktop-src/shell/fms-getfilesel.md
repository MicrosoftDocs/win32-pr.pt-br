---
description: Contém informações sobre um arquivo selecionado na janela do Gerenciador de arquivos ativo (a janela de diretório ou a janela de resultados da pesquisa).
title: Estrutura de FMS_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920625"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="e8a38-103">\_Estrutura GETFILESEL do FMS</span><span class="sxs-lookup"><span data-stu-id="e8a38-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="e8a38-104">Contém informações sobre um arquivo selecionado na janela do Gerenciador de arquivos ativo (a janela de diretório ou a janela de resultados da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="e8a38-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8a38-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="e8a38-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e8a38-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e8a38-107">**ftTime**</span><span class="sxs-lookup"><span data-stu-id="e8a38-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="e8a38-108">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="e8a38-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="e8a38-109">A hora e a data em que o arquivo foi criado.</span><span class="sxs-lookup"><span data-stu-id="e8a38-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="e8a38-110">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="e8a38-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="e8a38-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e8a38-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e8a38-112">O tamanho, em bytes, do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e8a38-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="e8a38-113">**rebatida**</span><span class="sxs-lookup"><span data-stu-id="e8a38-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="e8a38-114">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e8a38-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e8a38-115">Os atributos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e8a38-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="e8a38-116">**szName**</span><span class="sxs-lookup"><span data-stu-id="e8a38-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="e8a38-117">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="e8a38-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="e8a38-118">O caminho completo finalizado com nulo e o nome de arquivo do arquivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="e8a38-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8a38-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8a38-119">Requirements</span></span>



| <span data-ttu-id="e8a38-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a38-120">Requirement</span></span> | <span data-ttu-id="e8a38-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e8a38-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a38-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8a38-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a38-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8a38-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e8a38-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8a38-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a38-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8a38-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8a38-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8a38-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8a38-127"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8a38-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a38-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8a38-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a38-129">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="e8a38-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




