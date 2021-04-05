---
description: Habilita ou desabilita a leitura e a gravação de setores de disco.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: Função FveEnableRawAccessW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826281"
---
# <a name="fveenablerawaccessw-function"></a><span data-ttu-id="80664-103">Função FveEnableRawAccessW</span><span class="sxs-lookup"><span data-stu-id="80664-103">FveEnableRawAccessW function</span></span>

<span data-ttu-id="80664-104">Habilita ou desabilita a leitura e a gravação de setores de disco.</span><span class="sxs-lookup"><span data-stu-id="80664-104">Enables or disables reading and writing of disk sectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="80664-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80664-105">Syntax</span></span>


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="80664-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80664-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80664-107">*VolumeName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80664-107">*VolumeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80664-108">Um identificador exclusivo para o volume do disco.</span><span class="sxs-lookup"><span data-stu-id="80664-108">A unique identifier for the disk volume.</span></span>

</dd> <dt>

<span data-ttu-id="80664-109">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80664-109">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80664-110">Se **for true**, permitirá o acesso ao volume bruto.</span><span class="sxs-lookup"><span data-stu-id="80664-110">If **TRUE**, allows access to the raw volume.</span></span> <span data-ttu-id="80664-111">Se **for false**, nenhum acesso será permitido para o volume bruto.</span><span class="sxs-lookup"><span data-stu-id="80664-111">If **FALSE**, no access is allowed to the raw volume.</span></span> <span data-ttu-id="80664-112">Se o acesso bruto já tiver sido habilitado, mas esse valor for **false**, o volume será remontado e revalidado.</span><span class="sxs-lookup"><span data-stu-id="80664-112">If raw access has already been enabled but this value is **FALSE**, the volume is remounted and revalidated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80664-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80664-113">Return value</span></span>

<span data-ttu-id="80664-114">Essa função retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="80664-114">This function returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="80664-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="80664-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="80664-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="80664-116">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80664-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="80664-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                           | <span data-ttu-id="80664-118">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="80664-118">The function was successful.</span></span><br/>                                            |
| <dl> <span data-ttu-id="80664-119"><dt>**S \_ FALSO**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80664-119"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                        | <span data-ttu-id="80664-120">Habilitado é **falso** e o volume ainda não estava no modo de acesso bruto.</span><span class="sxs-lookup"><span data-stu-id="80664-120">Enabled is **FALSE** and the volume was not already in raw access mode.</span></span><br/> |
| <dl> <span data-ttu-id="80664-121"><dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="80664-121"><dt>**E\_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl> | <span data-ttu-id="80664-122">O volume não pode ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="80664-122">The volume cannot be locked.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="80664-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80664-123">Requirements</span></span>



| <span data-ttu-id="80664-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="80664-124">Requirement</span></span> | <span data-ttu-id="80664-125">Valor</span><span class="sxs-lookup"><span data-stu-id="80664-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80664-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80664-126">Minimum supported client</span></span><br/> | <span data-ttu-id="80664-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80664-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80664-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80664-128">Minimum supported server</span></span><br/> | <span data-ttu-id="80664-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80664-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80664-130">DLL</span><span class="sxs-lookup"><span data-stu-id="80664-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80664-131"><dt>Fveapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80664-131"><dt>Fveapi.dll</dt></span></span> </dl> |



 

 




