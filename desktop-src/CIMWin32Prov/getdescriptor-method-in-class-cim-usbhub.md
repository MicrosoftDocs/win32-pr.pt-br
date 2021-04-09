---
description: O método getdescriptor retorna o descritor do hub USB conforme especificado pelos parâmetros de entrada.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: Método getdescriptor da classe CIM_USBHub (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d68374b4a9267dbc50fbb5b2cd8f1f46018e7f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920291"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a><span data-ttu-id="9f73b-103">Método getdescriptor da classe CIM \_ USBHub</span><span class="sxs-lookup"><span data-stu-id="9f73b-103">GetDescriptor method of the CIM\_USBHub class</span></span>

<span data-ttu-id="9f73b-104">O método **getdescriptor** retorna o descritor do hub USB conforme especificado pelos parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="9f73b-104">The **GetDescriptor** method returns the USB hub descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f73b-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9f73b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9f73b-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9f73b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9f73b-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9f73b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9f73b-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9f73b-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f73b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f73b-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="9f73b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f73b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f73b-111">*RequestType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f73b-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f73b-112">Identificador mapeado por bit para o tipo de solicitação de descritor e o destinatário.</span><span class="sxs-lookup"><span data-stu-id="9f73b-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="9f73b-113">Para obter os valores apropriados para cada bit, consulte a especificação USB.</span><span class="sxs-lookup"><span data-stu-id="9f73b-113">For the appropriate values for each bit, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="9f73b-114">*RequestValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f73b-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f73b-115">Contém o tipo de descritor no alto byte e o índice de descritor (por exemplo, index ou offset na matriz de descritores) no byte baixo.</span><span class="sxs-lookup"><span data-stu-id="9f73b-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="9f73b-116">Para obter mais informações, consulte a especificação USB.</span><span class="sxs-lookup"><span data-stu-id="9f73b-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="9f73b-117">*RequestIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f73b-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f73b-118">Especifica o código do identificador de idioma de 2 bytes usado pelo dispositivo USB ao retornar dados do descritor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9f73b-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="9f73b-119">Normalmente, o parâmetro é 0 (zero) para descritores que não são de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9f73b-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="9f73b-120">Para obter mais informações, consulte a especificação USB.</span><span class="sxs-lookup"><span data-stu-id="9f73b-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="9f73b-121">*RequestLength* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9f73b-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f73b-122">Na entrada, o comprimento (em octetos) do descritor que deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="9f73b-122">On input, the length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="9f73b-123">Se esse valor for menor que o comprimento real do descritor, somente o comprimento solicitado será retornado.</span><span class="sxs-lookup"><span data-stu-id="9f73b-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="9f73b-124">Se for maior que o comprimento real, o comprimento real será retornado.</span><span class="sxs-lookup"><span data-stu-id="9f73b-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="9f73b-125">Na saída, o comprimento (em octetos) do buffer que está sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="9f73b-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="9f73b-126">Se o descritor solicitado não existir, o conteúdo desse parâmetro será indefinido.</span><span class="sxs-lookup"><span data-stu-id="9f73b-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="9f73b-127">*Buffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9f73b-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f73b-128">Buffer retorna as informações de descritor solicitadas.</span><span class="sxs-lookup"><span data-stu-id="9f73b-128">Buffer returns the requested descriptor information.</span></span> <span data-ttu-id="9f73b-129">Se o descritor não existir, o conteúdo do buffer será indefinido.</span><span class="sxs-lookup"><span data-stu-id="9f73b-129">If the descriptor does not exist, the contents of the buffer are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f73b-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f73b-130">Return value</span></span>

<span data-ttu-id="9f73b-131">Retorna um valor de 0 (zero) se o descritor de USB for retornado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="9f73b-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="9f73b-132">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método.</span><span class="sxs-lookup"><span data-stu-id="9f73b-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="9f73b-133">As cadeias de caracteres para as quais os conteúdos de **mofqualifier** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .</span><span class="sxs-lookup"><span data-stu-id="9f73b-133">The strings to which the **mofqualifier** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f73b-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f73b-134">Remarks</span></span>

<span data-ttu-id="9f73b-135">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9f73b-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9f73b-136">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="9f73b-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9f73b-137">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9f73b-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9f73b-138">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f73b-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f73b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f73b-139">Requirements</span></span>



| <span data-ttu-id="9f73b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f73b-140">Requirement</span></span> | <span data-ttu-id="9f73b-141">Valor</span><span class="sxs-lookup"><span data-stu-id="9f73b-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f73b-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f73b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9f73b-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f73b-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f73b-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f73b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9f73b-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f73b-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f73b-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f73b-146">Namespace</span></span><br/>                | <span data-ttu-id="9f73b-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9f73b-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f73b-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f73b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f73b-149"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f73b-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="9f73b-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9f73b-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f73b-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f73b-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f73b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9f73b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f73b-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f73b-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f73b-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f73b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f73b-155">**CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="9f73b-155">**CIM\_USBHub**</span></span>](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[<span data-ttu-id="9f73b-156">**CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="9f73b-156">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> </dl>

 

