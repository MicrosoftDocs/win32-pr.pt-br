---
description: Retorna o descritor USBDevice conforme especificado pelos parâmetros de entrada.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Método getdescriptor da classe CIM_USBDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756770"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="13b2d-103">Método getdescriptor da classe CIM_USBDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="13b2d-103">GetDescriptor method of the CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="13b2d-104">Retorna o descritor USBDevice conforme especificado pelos parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="13b2d-104">Returns the USBDevice descriptor as specified by the input parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b2d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13b2d-105">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="13b2d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13b2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13b2d-107">*RequestType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="13b2d-107">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13b2d-108">Mapa de bits que identifica o tipo de solicitação de descritor e o destinatário.</span><span class="sxs-lookup"><span data-stu-id="13b2d-108">Bit-map that identifies the type of Descriptor request and the recipient.</span></span> <span data-ttu-id="13b2d-109">O tipo de solicitação pode ser ' padrão ', ' classe ' ou ' específico do fornecedor '.</span><span class="sxs-lookup"><span data-stu-id="13b2d-109">The type of request may be 'standard', 'class' or 'vendor-specific'.</span></span> <span data-ttu-id="13b2d-110">O destinatário pode ser ' dispositivo ', ' interface ', ' ponto de extremidade ' ou ' outros '.</span><span class="sxs-lookup"><span data-stu-id="13b2d-110">The recipient may be 'device', 'interface', 'endpoint' or 'other'.</span></span> <span data-ttu-id="13b2d-111">Consulte a especificação USB para obter os valores apropriados para cada bit.</span><span class="sxs-lookup"><span data-stu-id="13b2d-111">Refer to the USB Specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="13b2d-112">*RequestValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="13b2d-112">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13b2d-113">Contém o tipo de descritor no alto byte e o índice de descritor (por exemplo, index ou offset na matriz de descritores) no byte baixo.</span><span class="sxs-lookup"><span data-stu-id="13b2d-113">Contains the Descriptor Type in the high byte and the Descriptor Index (for example, index or offset into the Descriptor array) in the low byte.</span></span> <span data-ttu-id="13b2d-114">Consulte a especificação USB para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13b2d-114">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="13b2d-115">*RequestIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="13b2d-115">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13b2d-116">Define o código de ID de idioma de 2 bytes usado pelo USBDevice ao retornar dados de descritor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="13b2d-116">Defines the 2 byte Language ID code used by the USBDevice when returning string Descriptor data.</span></span> <span data-ttu-id="13b2d-117">O parâmetro geralmente é 0 para descritores que não são de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="13b2d-117">The parameter is typically 0 for non-string Descriptors.</span></span> <span data-ttu-id="13b2d-118">Consulte a especificação USB para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13b2d-118">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="13b2d-119">*RequestLength* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="13b2d-119">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b2d-120">Na entrada, contém o comprimento (em octetos) do descritor que deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="13b2d-120">On input, contains the length (in octets) of the Descriptor that should be returned.</span></span> <span data-ttu-id="13b2d-121">Se esse valor for menor que o comprimento real do descritor, somente o comprimento solicitado será retornado.</span><span class="sxs-lookup"><span data-stu-id="13b2d-121">If this value is less than the actual length of the Descriptor, only the requested length will be returned.</span></span> <span data-ttu-id="13b2d-122">Se for maior que o comprimento real, o comprimento real será retornado.</span><span class="sxs-lookup"><span data-stu-id="13b2d-122">If it is more than the actual length, the actual length is returned.</span></span> <span data-ttu-id="13b2d-123">Na saída, esse parâmetro é o comprimento, em octetos, do buffer que está sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="13b2d-123">On output, this parameter is the length, in octets, of the Buffer being returned.</span></span> <span data-ttu-id="13b2d-124">Se o descritor solicitado não existir, o conteúdo desse parâmetro será indefinido.</span><span class="sxs-lookup"><span data-stu-id="13b2d-124">If the requested Descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="13b2d-125">*Buffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="13b2d-125">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b2d-126">Retorna as informações de descritor solicitadas.</span><span class="sxs-lookup"><span data-stu-id="13b2d-126">Returns the requested Descriptor information.</span></span> <span data-ttu-id="13b2d-127">Se o descritor não existir, o conteúdo do parâmetro será indefinido.</span><span class="sxs-lookup"><span data-stu-id="13b2d-127">If the Descriptor does not exist, the contents of the parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13b2d-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13b2d-128">Return value</span></span>

<span data-ttu-id="13b2d-129">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="13b2d-129">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b2d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13b2d-130">Requirements</span></span>



| <span data-ttu-id="13b2d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="13b2d-131">Requirement</span></span> | <span data-ttu-id="13b2d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="13b2d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b2d-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13b2d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="13b2d-134">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13b2d-134">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="13b2d-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13b2d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="13b2d-136">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="13b2d-136">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="13b2d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="13b2d-137">Namespace</span></span><br/>                | <span data-ttu-id="13b2d-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="13b2d-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13b2d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="13b2d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13b2d-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13b2d-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13b2d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="13b2d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b2d-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13b2d-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13b2d-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="13b2d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b2d-144">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="13b2d-144">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

 




