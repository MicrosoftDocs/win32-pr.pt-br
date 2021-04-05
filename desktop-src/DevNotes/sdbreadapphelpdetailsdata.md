---
Description: Recupera dados do banco de dado detalhes de AppHelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: Função SdbReadApphelpDetailsData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918383"
---
# <a name="sdbreadapphelpdetailsdata-function"></a><span data-ttu-id="50417-103">Função SdbReadApphelpDetailsData</span><span class="sxs-lookup"><span data-stu-id="50417-103">SdbReadApphelpDetailsData function</span></span>

<span data-ttu-id="50417-104">Recupera dados do banco de dado detalhes de AppHelp.</span><span class="sxs-lookup"><span data-stu-id="50417-104">Retrieves data from the Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="50417-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50417-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="50417-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50417-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50417-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50417-108">Um identificador para o banco de dados de detalhes AppHelp, AppHelp. sdb.</span><span class="sxs-lookup"><span data-stu-id="50417-108">A handle to the Apphelp details database, Apphelp.sdb.</span></span>

</dd> <dt>

<span data-ttu-id="50417-109">*pData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="50417-109">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50417-110">Uma estrutura de [**\_ dados APPHELP**](apphelp-data.md) .</span><span class="sxs-lookup"><span data-stu-id="50417-110">An [**APPHELP\_DATA**](apphelp-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50417-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50417-111">Return value</span></span>

<span data-ttu-id="50417-112">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="50417-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="50417-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50417-113">Requirements</span></span>



| <span data-ttu-id="50417-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50417-114">Requirement</span></span> | <span data-ttu-id="50417-115">Valor</span><span class="sxs-lookup"><span data-stu-id="50417-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50417-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50417-116">Minimum supported client</span></span><br/> | <span data-ttu-id="50417-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50417-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="50417-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50417-118">Minimum supported server</span></span><br/> | <span data-ttu-id="50417-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50417-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="50417-120">DLL</span><span class="sxs-lookup"><span data-stu-id="50417-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50417-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50417-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




