---
description: O método getdescriptor retorna o descritor de dispositivo USB conforme especificado pelos parâmetros de entrada.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: Método getdescriptor da classe CIM_USBDevice (Wmcodecdsp. h)
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
- CIMWin32.dll
ms.openlocfilehash: 35ce9a83efb580d6e5e44f55a01182e7390c120e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755198"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a><span data-ttu-id="053d3-103">Método getdescriptor da classe CIM_USBDevice (Wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="053d3-103">GetDescriptor method of the CIM_USBDevice class (Wmcodecdsp.h)</span></span>

<span data-ttu-id="053d3-104">O método **getdescriptor** retorna o descritor de dispositivo USB conforme especificado pelos parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="053d3-104">The **GetDescriptor** method returns the USB device descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="053d3-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="053d3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="053d3-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="053d3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="053d3-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="053d3-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="053d3-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="053d3-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="053d3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="053d3-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="053d3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="053d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="053d3-111">*RequestType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="053d3-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="053d3-112">Identificador mapeado por bit para o tipo de solicitação de descritor e o destinatário.</span><span class="sxs-lookup"><span data-stu-id="053d3-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="053d3-113">Consulte a especificação USB para obter os valores apropriados para cada bit.</span><span class="sxs-lookup"><span data-stu-id="053d3-113">Refer to the USB specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="053d3-114">*RequestValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="053d3-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="053d3-115">Contém o tipo de descritor no alto byte e o índice de descritor (por exemplo, index ou offset na matriz de descritores) no byte baixo.</span><span class="sxs-lookup"><span data-stu-id="053d3-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="053d3-116">Para obter mais informações, consulte a especificação USB.</span><span class="sxs-lookup"><span data-stu-id="053d3-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="053d3-117">*RequestIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="053d3-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="053d3-118">Especifica o código do identificador de idioma de 2 bytes usado pelo dispositivo USB ao retornar dados do descritor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="053d3-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="053d3-119">Normalmente, o parâmetro é 0 (zero) para descritores que não são de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="053d3-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="053d3-120">Para obter mais informações, consulte a especificação USB.</span><span class="sxs-lookup"><span data-stu-id="053d3-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="053d3-121">*RequestLength* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="053d3-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="053d3-122">Na entrada, comprimento (em octetos) do descritor que deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="053d3-122">On input, length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="053d3-123">Se esse valor for menor que o comprimento real do descritor, somente o comprimento solicitado será retornado.</span><span class="sxs-lookup"><span data-stu-id="053d3-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="053d3-124">Se for maior que o comprimento real, o comprimento real será retornado.</span><span class="sxs-lookup"><span data-stu-id="053d3-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="053d3-125">Na saída, o comprimento (em octetos) do buffer que está sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="053d3-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="053d3-126">Se o descritor solicitado não existir, o conteúdo desse parâmetro será indefinido.</span><span class="sxs-lookup"><span data-stu-id="053d3-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="053d3-127">*Buffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="053d3-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="053d3-128">Retorna as informações de descritor solicitadas.</span><span class="sxs-lookup"><span data-stu-id="053d3-128">Returns the requested descriptor information.</span></span> <span data-ttu-id="053d3-129">Se o descritor não existir, o conteúdo desse parâmetro será indefinido.</span><span class="sxs-lookup"><span data-stu-id="053d3-129">If the descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="053d3-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="053d3-130">Return value</span></span>

<span data-ttu-id="053d3-131">Retorna um valor de 0 (zero) se o descritor de USB for retornado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="053d3-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="053d3-132">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="053d3-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="053d3-133">As cadeias de caracteres para as quais os conteúdos de mofqualifier são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="053d3-133">The strings to which the mofqualifier contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="053d3-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="053d3-134">Remarks</span></span>

<span data-ttu-id="053d3-135">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="053d3-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="053d3-136">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="053d3-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="053d3-137">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="053d3-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="053d3-138">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="053d3-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="053d3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="053d3-139">Requirements</span></span>



| <span data-ttu-id="053d3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="053d3-140">Requirement</span></span> | <span data-ttu-id="053d3-141">Valor</span><span class="sxs-lookup"><span data-stu-id="053d3-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="053d3-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="053d3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="053d3-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="053d3-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="053d3-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="053d3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="053d3-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="053d3-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="053d3-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="053d3-146">Namespace</span></span><br/>                | <span data-ttu-id="053d3-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="053d3-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="053d3-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="053d3-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="053d3-149"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="053d3-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="053d3-150">MOF</span><span class="sxs-lookup"><span data-stu-id="053d3-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="053d3-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="053d3-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="053d3-152">DLL</span><span class="sxs-lookup"><span data-stu-id="053d3-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="053d3-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="053d3-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="053d3-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="053d3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="053d3-155">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="053d3-155">**CIM\_USBDevice**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[<span data-ttu-id="053d3-156">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="053d3-156">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

