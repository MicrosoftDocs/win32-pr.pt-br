---
description: Contém informações sobre um arquivo selecionado na janela ativa do Gerenciador de Arquivos (a janela diretório ou a janela Resultados da Pesquisa).
title: FMS_GETFILESEL (Wfext.h)
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
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842217"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="b6b5a-103">Estrutura \_ GETFILESEL DO FMS</span><span class="sxs-lookup"><span data-stu-id="b6b5a-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="b6b5a-104">Contém informações sobre um arquivo selecionado na janela ativa do Gerenciador de Arquivos (a janela diretório ou a janela Resultados da Pesquisa).</span><span class="sxs-lookup"><span data-stu-id="b6b5a-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b5a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6b5a-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="b6b5a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b6b5a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b6b5a-107">**ftTime**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="b6b5a-108">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="b6b5a-109">A hora e a data em que o arquivo foi criado.</span><span class="sxs-lookup"><span data-stu-id="b6b5a-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="b6b5a-110">**Dwsize**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b6b5a-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="b6b5a-112">O tamanho, em bytes, do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6b5a-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="b6b5a-113">**bAttr**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="b6b5a-114">Tipo: **BYTE**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="b6b5a-115">Os atributos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6b5a-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="b6b5a-116">**Szname**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="b6b5a-117">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="b6b5a-118">O caminho completo com terminação nula e o nome do arquivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="b6b5a-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6b5a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6b5a-119">Requirements</span></span>



| <span data-ttu-id="b6b5a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6b5a-120">Requirement</span></span> | <span data-ttu-id="b6b5a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b6b5a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b5a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6b5a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b5a-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b6b5a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b6b5a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6b5a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b5a-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b6b5a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b6b5a-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b6b5a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b5a-127"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b5a-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6b5a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6b5a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b5a-129">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="b6b5a-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




