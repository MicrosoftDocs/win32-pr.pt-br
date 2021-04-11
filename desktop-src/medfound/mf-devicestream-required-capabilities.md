---
description: Especifica uma lista de cadeias de caracteres Unicode que representam os recursos do dispositivo exigidos pela transformação do sensor.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: Atributo MF_DEVICESTREAM_REQUIRED_CAPABILITIES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090691"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a><span data-ttu-id="369cd-103">\_Atributo de \_ \_ funcionalidades necessárias do MF DEVICESTREAM</span><span class="sxs-lookup"><span data-stu-id="369cd-103">MF\_DEVICESTREAM\_REQUIRED\_CAPABILITIES attribute</span></span>

<span data-ttu-id="369cd-104">Especifica uma lista de cadeias de caracteres Unicode que representam os recursos do dispositivo exigidos pela transformação do sensor.</span><span class="sxs-lookup"><span data-stu-id="369cd-104">Specifies a list of unicode strings representing the device capabilities required by the sensor transform.</span></span>

## <a name="data-type"></a><span data-ttu-id="369cd-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="369cd-105">Data type</span></span>

<span data-ttu-id="369cd-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="369cd-106">\**WCHAR\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="369cd-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="369cd-107">Remarks</span></span>

<span data-ttu-id="369cd-108">Esse atributo é opcional e só será necessário se a transformação do sensor acessar um recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="369cd-108">This attribute is optional and only required if the sensor transform accesses a protected resource.</span></span> <span data-ttu-id="369cd-109">O valor deve ser uma lista delimitada por ponto e vírgula de tokens de cadeia de caracteres definidos em [_ *DeviceCapability* \*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span><span class="sxs-lookup"><span data-stu-id="369cd-109">The value must be a semicolon delimited list of string tokens defined in [_ *DeviceCapability*\*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span></span>

## <a name="requirements"></a><span data-ttu-id="369cd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="369cd-110">Requirements</span></span>



| <span data-ttu-id="369cd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="369cd-111">Requirement</span></span> | <span data-ttu-id="369cd-112">Valor</span><span class="sxs-lookup"><span data-stu-id="369cd-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="369cd-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="369cd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="369cd-114">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="369cd-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="369cd-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="369cd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="369cd-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="369cd-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="369cd-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="369cd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="369cd-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="369cd-118"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
