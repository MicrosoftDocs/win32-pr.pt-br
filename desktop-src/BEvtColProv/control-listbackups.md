---
description: Retorna a lista dos arquivos de configuração de backup salvos que podem ser restaurados.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Método ListBackups da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088884"
---
# <a name="listbackups-method-of-the-control-class"></a><span data-ttu-id="64216-103">Método ListBackups da classe Control</span><span class="sxs-lookup"><span data-stu-id="64216-103">ListBackups method of the Control class</span></span>

<span data-ttu-id="64216-104">Retorna a lista dos arquivos de configuração de backup salvos que podem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="64216-104">Returns the list of the saved backup configuration files that can be restored.</span></span>

## <a name="syntax"></a><span data-ttu-id="64216-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64216-105">Syntax</span></span>


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a><span data-ttu-id="64216-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64216-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64216-107">*OriginalTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="64216-107">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64216-108">O carimbo de data/hora de quando a configuração atual foi definida (se restaurada do backup, conterá o carimbo de data/hora original).</span><span class="sxs-lookup"><span data-stu-id="64216-108">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="64216-109">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="64216-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="64216-110">*OriginalTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="64216-110">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64216-111">O carimbo de data/hora de quando a configuração atual foi definida (se restaurada do backup, conterá o carimbo de data/hora original).</span><span class="sxs-lookup"><span data-stu-id="64216-111">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="64216-112">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="64216-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="64216-113">*Arquivos* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="64216-113">*Files* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64216-114">A lista de arquivos de backup disponíveis, na ordem do mais recente ao mais antigo.</span><span class="sxs-lookup"><span data-stu-id="64216-114">The list of available backup files, in order from the newest to the oldest.</span></span>

</dd> <dt>

<span data-ttu-id="64216-115">*FilesTimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="64216-115">*FilesTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64216-116">Para cada arquivo de backup, o carimbo de data/hora de quando sua configuração foi definida.</span><span class="sxs-lookup"><span data-stu-id="64216-116">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="64216-117">Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="64216-117">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="64216-118">*FilesTimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="64216-118">*FilesTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64216-119">Para cada arquivo de backup, o carimbo de data/hora de quando sua configuração foi definida.</span><span class="sxs-lookup"><span data-stu-id="64216-119">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="64216-120">Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="64216-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64216-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64216-121">Return value</span></span>

<span data-ttu-id="64216-122">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="64216-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="64216-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64216-123">Requirements</span></span>



| <span data-ttu-id="64216-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="64216-124">Requirement</span></span> | <span data-ttu-id="64216-125">Valor</span><span class="sxs-lookup"><span data-stu-id="64216-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64216-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64216-126">Minimum supported client</span></span><br/> | <span data-ttu-id="64216-127">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="64216-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="64216-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64216-128">Minimum supported server</span></span><br/> | <span data-ttu-id="64216-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="64216-129">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="64216-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="64216-130">Namespace</span></span><br/>                | <span data-ttu-id="64216-131">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="64216-131">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="64216-132">MOF</span><span class="sxs-lookup"><span data-stu-id="64216-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64216-133"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64216-133"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="64216-134">DLL</span><span class="sxs-lookup"><span data-stu-id="64216-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64216-135"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64216-135"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="64216-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="64216-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64216-137">**Controlo**</span><span class="sxs-lookup"><span data-stu-id="64216-137">**Control**</span></span>](control.md)
</dt> </dl>

 

