---
description: Inicializa ou reinicializa a lista de imagens do sistema.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: Função FileIconInit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296732"
---
# <a name="fileiconinit-function"></a><span data-ttu-id="f834a-103">Função FileIconInit</span><span class="sxs-lookup"><span data-stu-id="f834a-103">FileIconInit function</span></span>

<span data-ttu-id="f834a-104">Inicializa ou reinicializa a lista de imagens do sistema.</span><span class="sxs-lookup"><span data-stu-id="f834a-104">Initializes or reinitializes the system image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f834a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f834a-105">Syntax</span></span>


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a><span data-ttu-id="f834a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f834a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f834a-107">*fRestoreCache* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f834a-107">*fRestoreCache* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f834a-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="f834a-108">Type: **BOOL**</span></span>

<span data-ttu-id="f834a-109">**True** para restaurar o cache de imagem do sistema do disco; Caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="f834a-109">**TRUE** to restore the system image cache from disk; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f834a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f834a-110">Return value</span></span>

<span data-ttu-id="f834a-111">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="f834a-111">Type: **BOOL**</span></span>

<span data-ttu-id="f834a-112">**True** se o cache tiver sido atualizado com êxito, **false** se a inicialização falhou.</span><span class="sxs-lookup"><span data-stu-id="f834a-112">**TRUE** if the cache was successfully refreshed, **FALSE** if the initialization failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f834a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f834a-113">Remarks</span></span>

<span data-ttu-id="f834a-114">Se você estiver usando listas de imagens do sistema em seu próprio processo, deverá chamar **FileIconInit** nos seguintes horários:</span><span class="sxs-lookup"><span data-stu-id="f834a-114">If you are using system image lists in your own process, you must call **FileIconInit** at the following times:</span></span>

-   <span data-ttu-id="f834a-115">Na inicialização.</span><span class="sxs-lookup"><span data-stu-id="f834a-115">On launch.</span></span>
-   <span data-ttu-id="f834a-116">Em resposta a uma mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) quando o sinalizador [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) é definido.</span><span class="sxs-lookup"><span data-stu-id="f834a-116">In response to a [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message when the [**SPI\_SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) flag is set.</span></span>

<span data-ttu-id="f834a-117">**FileIconInit** não está incluído em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="f834a-117">**FileIconInit** is not included in a header file.</span></span> <span data-ttu-id="f834a-118">Você deve chamá-lo diretamente do Shell32.dll, usando o ordinal 660.</span><span class="sxs-lookup"><span data-stu-id="f834a-118">You must call it directly from Shell32.dll, using ordinal 660.</span></span>

## <a name="requirements"></a><span data-ttu-id="f834a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f834a-119">Requirements</span></span>



| <span data-ttu-id="f834a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f834a-120">Requirement</span></span> | <span data-ttu-id="f834a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f834a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f834a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f834a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f834a-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f834a-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f834a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f834a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f834a-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f834a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f834a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f834a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f834a-127"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f834a-127"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
