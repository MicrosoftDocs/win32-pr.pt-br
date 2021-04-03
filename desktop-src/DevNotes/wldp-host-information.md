---
description: Uma estrutura que identifica o host e o arquivo de origem a serem avaliados.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: Estrutura de WLDP_HOST_INFORMATION (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010101"
---
# <a name="wldp_host_information-structure"></a><span data-ttu-id="b5e7f-103">Estrutura de informações do \_ host WLDP \_</span><span class="sxs-lookup"><span data-stu-id="b5e7f-103">WLDP\_HOST\_INFORMATION structure</span></span>

<span data-ttu-id="b5e7f-104">Uma estrutura que identifica o host e o arquivo de origem a serem avaliados.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-104">A structure identifying the host and source file to be evaluated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5e7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5e7f-105">Syntax</span></span>


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="b5e7f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b5e7f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5e7f-107">**dwRevision**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-107">**dwRevision**</span></span>
</dt> <dd>

<span data-ttu-id="b5e7f-108">Deve ser **a \_ \_ \_ revisão de informações do host WLDP**.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-108">Must be **WLDP\_HOST\_INFORMATION\_REVISION**.</span></span>

</dd> <dt>

<span data-ttu-id="b5e7f-109">**dwHostId**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-109">**dwHostId**</span></span>
</dt> <dd>

<span data-ttu-id="b5e7f-110">Valor de enumeração [**da \_ \_ ID de host WLDP**](wldp-host-id.md) que descreve a ID do host.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-110">Enumeration value from [**WLDP\_HOST\_ID**](wldp-host-id.md) that describes the host ID.</span></span>

</dd> <dt>

<span data-ttu-id="b5e7f-111">**szSource**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-111">**szSource**</span></span>
</dt> <dd>

<span data-ttu-id="b5e7f-112">Caminho completo e nome do script com a extensão.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-112">Full path and script name with the extension.</span></span> <span data-ttu-id="b5e7f-113">NULL para **WLDP \_ de \_ ID \_ de host global** ou execução de script manual.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-113">NULL for **WLDP\_HOST\_ID\_GLOBAL**, or manual script execution.</span></span>

</dd> <dt>

<span data-ttu-id="b5e7f-114">**hSource**</span><span class="sxs-lookup"><span data-stu-id="b5e7f-114">**hSource**</span></span>
</dt> <dd>

<span data-ttu-id="b5e7f-115">Além do nome, o chamador pode especificar um identificador para o arquivo usado para validação.</span><span class="sxs-lookup"><span data-stu-id="b5e7f-115">In addition to the name, the caller can specify a handle to the file used for validation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5e7f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5e7f-116">Requirements</span></span>



| <span data-ttu-id="b5e7f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5e7f-117">Requirement</span></span> | <span data-ttu-id="b5e7f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b5e7f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e7f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5e7f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5e7f-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b5e7f-120">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5e7f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5e7f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5e7f-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b5e7f-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b5e7f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5e7f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5e7f-124"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5e7f-124"><dt>Wldp.h</dt></span></span> </dl> |



 

 




