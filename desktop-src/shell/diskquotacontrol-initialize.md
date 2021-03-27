---
description: Abre um volume especificado e inicializa seu objeto de controle de cota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Inimétodo tialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967306"
---
# <a name="diskquotacontrolinitialize-method"></a><span data-ttu-id="70bbe-103">DiskQuotaControl.Inimétodo tialize</span><span class="sxs-lookup"><span data-stu-id="70bbe-103">DiskQuotaControl.Initialize method</span></span>

<span data-ttu-id="70bbe-104">Abre um volume especificado e inicializa seu objeto de controle de cota.</span><span class="sxs-lookup"><span data-stu-id="70bbe-104">Opens a specified volume and initializes its quota control object.</span></span>

## <a name="syntax"></a><span data-ttu-id="70bbe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70bbe-105">Syntax</span></span>


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a><span data-ttu-id="70bbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70bbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70bbe-107">*sPath*</span><span class="sxs-lookup"><span data-stu-id="70bbe-107">*sPath*</span></span> 
</dt> <dd>

<span data-ttu-id="70bbe-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70bbe-108">Type: **String**</span></span>

<span data-ttu-id="70bbe-109">Um valor de cadeia de caracteres que contém o caminho totalmente qualificado do volume a ser inicializado.</span><span class="sxs-lookup"><span data-stu-id="70bbe-109">A string value that contains the fully qualified path of the volume to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="70bbe-110">*bReadWrite*</span><span class="sxs-lookup"><span data-stu-id="70bbe-110">*bReadWrite*</span></span> 
</dt> <dd>

<span data-ttu-id="70bbe-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="70bbe-111">Type: **Boolean**</span></span>

<span data-ttu-id="70bbe-112">Um valor booliano que especifica como o volume deve ser aberto.</span><span class="sxs-lookup"><span data-stu-id="70bbe-112">A Boolean value that specifies how the volume is to be opened.</span></span> <span data-ttu-id="70bbe-113">Defina *bReadWrite* como **true** para acesso de leitura/gravação ou **false** para acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="70bbe-113">Set *bReadWrite* to **TRUE** for read/write access or **FALSE** for read-only access.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70bbe-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70bbe-114">Return value</span></span>

<span data-ttu-id="70bbe-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="70bbe-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="70bbe-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70bbe-116">Requirements</span></span>



| <span data-ttu-id="70bbe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="70bbe-117">Requirement</span></span> | <span data-ttu-id="70bbe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="70bbe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70bbe-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70bbe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="70bbe-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="70bbe-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70bbe-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70bbe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="70bbe-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="70bbe-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="70bbe-123">DLL</span><span class="sxs-lookup"><span data-stu-id="70bbe-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70bbe-124"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="70bbe-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70bbe-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="70bbe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70bbe-126">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="70bbe-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




