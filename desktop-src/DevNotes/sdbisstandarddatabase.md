---
description: Determina se o banco de dados especificado é um dos bancos de dados padrão (SysMain, AppHelp, Drvmain ou Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: Função SdbIsStandardDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010085"
---
# <a name="sdbisstandarddatabase-function"></a><span data-ttu-id="28c9a-103">Função SdbIsStandardDatabase</span><span class="sxs-lookup"><span data-stu-id="28c9a-103">SdbIsStandardDatabase function</span></span>

<span data-ttu-id="28c9a-104">Determina se o banco de dados especificado é um dos bancos de dados padrão (SysMain, AppHelp, Drvmain ou Msimain).</span><span class="sxs-lookup"><span data-stu-id="28c9a-104">Determines whether the specified database is one of the standard databases (Sysmain, Apphelp, Drvmain, or Msimain).</span></span>

## <a name="syntax"></a><span data-ttu-id="28c9a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28c9a-105">Syntax</span></span>


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a><span data-ttu-id="28c9a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28c9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c9a-107">*GuidDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28c9a-107">*GuidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c9a-108">O GUID do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="28c9a-108">The GUID for the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c9a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28c9a-109">Return value</span></span>

<span data-ttu-id="28c9a-110">A função retornará **true** se o GUID representar um banco de dados padrão ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="28c9a-110">The function returns **TRUE** if the GUID represents a standard database or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c9a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c9a-111">Requirements</span></span>



| <span data-ttu-id="28c9a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c9a-112">Requirement</span></span> | <span data-ttu-id="28c9a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="28c9a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28c9a-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28c9a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="28c9a-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28c9a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="28c9a-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28c9a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="28c9a-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28c9a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="28c9a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="28c9a-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28c9a-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28c9a-119"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




