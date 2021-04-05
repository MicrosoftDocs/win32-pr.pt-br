---
description: A função InstallWiaDevice instala um dispositivo de aquisição de imagem do Windows (WIA) como dispositivo enumerado por raiz. Ele poderá avisar um aviso de segurança se qualquer arquivo de instalação ou o instalador não for assinado digitalmente e confiável.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Função InstallWiaDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647490"
---
# <a name="installwiadevice-function"></a><span data-ttu-id="b9063-104">Função InstallWiaDevice</span><span class="sxs-lookup"><span data-stu-id="b9063-104">InstallWiaDevice function</span></span>

<span data-ttu-id="b9063-105">A função **InstallWiaDevice** instala um dispositivo de aquisição de imagem do Windows (WIA) como dispositivo enumerado por raiz.</span><span class="sxs-lookup"><span data-stu-id="b9063-105">The **InstallWiaDevice** function installs a Windows Image Acquisition (WIA) device as root-enumerated device.</span></span> <span data-ttu-id="b9063-106">Ele poderá avisar um aviso de segurança se qualquer arquivo de instalação ou o instalador não for assinado digitalmente e confiável.</span><span class="sxs-lookup"><span data-stu-id="b9063-106">It may popup a security warning if any installing file or coinstaller is not digitally signed and trusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9063-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9063-107">Syntax</span></span>


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a><span data-ttu-id="b9063-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9063-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9063-109">*pWiaDeviceInstall* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9063-109">*pWiaDeviceInstall* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9063-110">Tipo: \**PWIADEVICEINSTALL \** _</span><span class="sxs-lookup"><span data-stu-id="b9063-110">Type: \**PWIADEVICEINSTALL\** _</span></span>

<span data-ttu-id="b9063-111">Ponteiro para uma estrutura WIADEVICEINSTALL.</span><span class="sxs-lookup"><span data-stu-id="b9063-111">Pointer to a WIADEVICEINSTALL structure.</span></span> <span data-ttu-id="b9063-112">O membro _szFriendlyName \* da estrutura deve ser definido como o dispositivo FriendlyName real.</span><span class="sxs-lookup"><span data-stu-id="b9063-112">The _szFriendlyName\* member of the structure must be set to the actual device FriendlyName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9063-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9063-113">Return value</span></span>

<span data-ttu-id="b9063-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b9063-114">Type: **DWORD**</span></span>

<span data-ttu-id="b9063-115">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="b9063-115">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b9063-116">Se a função falhar, ela retornará um código de erro Win32.</span><span class="sxs-lookup"><span data-stu-id="b9063-116">If the function fails, it returns a Win32 error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9063-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9063-117">Requirements</span></span>



| <span data-ttu-id="b9063-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9063-118">Requirement</span></span> | <span data-ttu-id="b9063-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b9063-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9063-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9063-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b9063-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9063-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b9063-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9063-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b9063-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9063-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b9063-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9063-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9063-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9063-125"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b9063-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9063-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9063-127"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9063-127"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




