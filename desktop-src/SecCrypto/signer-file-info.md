---
description: Especifica um arquivo a ser assinado.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Estrutura de SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766818"
---
# <a name="signer_file_info-structure"></a><span data-ttu-id="1d805-103">Estrutura de informações do \_ arquivo de signatário \_</span><span class="sxs-lookup"><span data-stu-id="1d805-103">SIGNER\_FILE\_INFO structure</span></span>

<span data-ttu-id="1d805-104">A estrutura de **\_ \_ informações do arquivo de signatário** especifica um arquivo a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="1d805-104">The **SIGNER\_FILE\_INFO** structure specifies a file to sign.</span></span>

> [!Note]  
> <span data-ttu-id="1d805-105">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="1d805-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="1d805-106">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="1d805-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1d805-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d805-107">Syntax</span></span>


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a><span data-ttu-id="1d805-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1d805-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d805-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="1d805-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="1d805-110">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="1d805-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="1d805-111">**pwszFileName**</span><span class="sxs-lookup"><span data-stu-id="1d805-111">**pwszFileName**</span></span>
</dt> <dd>

<span data-ttu-id="1d805-112">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do arquivo a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="1d805-112">A pointer to a null-terminated string that contains the name of the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="1d805-113">**hFile**</span><span class="sxs-lookup"><span data-stu-id="1d805-113">**hFile**</span></span>
</dt> <dd>

<span data-ttu-id="1d805-114">Um identificador aberto para o arquivo especificado pelo membro **pwszFileName** .</span><span class="sxs-lookup"><span data-stu-id="1d805-114">An open handle to the file specified by the **pwszFileName** member.</span></span> <span data-ttu-id="1d805-115">Se esse membro contiver um identificador válido, esse identificador será usado para acessar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1d805-115">If this member contains a valid handle, this handle is used to access the file.</span></span> <span data-ttu-id="1d805-116">Esse membro pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1d805-116">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d805-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d805-117">Requirements</span></span>



| <span data-ttu-id="1d805-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d805-118">Requirement</span></span> | <span data-ttu-id="1d805-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1d805-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1d805-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d805-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d805-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1d805-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1d805-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d805-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d805-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d805-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d805-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d805-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d805-125">**\_informações de assunto do assinante \_**</span><span class="sxs-lookup"><span data-stu-id="1d805-125">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 




