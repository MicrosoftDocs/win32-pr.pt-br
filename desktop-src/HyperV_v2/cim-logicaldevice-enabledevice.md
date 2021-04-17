---
description: O método EnableDevice foi preterido no lugar do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Método EnableDevice da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787529"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="66639-103">Método EnableDevice da classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="66639-103">EnableDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="66639-104">O método EnableDevice foi preterido no lugar do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.</span><span class="sxs-lookup"><span data-stu-id="66639-104">The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.</span></span>

<span data-ttu-id="66639-105">Solicita que o LogicalDevice esteja habilitado ("Enabled" parâmetro de entrada = TRUE) ou Disabled (= FALSE).</span><span class="sxs-lookup"><span data-stu-id="66639-105">Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE).</span></span> <span data-ttu-id="66639-106">Se for bem-sucedido, as propriedades StatusInfo/Enabledstate do dispositivo deverão refletir o estado desejado (habilitado/desabilitado).</span><span class="sxs-lookup"><span data-stu-id="66639-106">If successful, the Device's StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled).</span></span> <span data-ttu-id="66639-107">Observe que a função desse método se sobrepõe à propriedade Requestedstate.</span><span class="sxs-lookup"><span data-stu-id="66639-107">Note that this method's function overlaps with the RequestedState property.</span></span> <span data-ttu-id="66639-108">O requestedstate foi adicionado ao modelo para manter um registro (ou seja, um valor persistente) da última solicitação de estado.</span><span class="sxs-lookup"><span data-stu-id="66639-108">RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request.</span></span> <span data-ttu-id="66639-109">Invocar o método EnableDevice deve definir a propriedade Requestedstate corretamente.</span><span class="sxs-lookup"><span data-stu-id="66639-109">Invoking the EnableDevice method should set the RequestedState property appropriately.</span></span>

<span data-ttu-id="66639-110">O código de retorno deverá ser 0 se a solicitação tiver sido executada com êxito, 1 se a solicitação não tiver suporte e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="66639-110">The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred.</span></span> <span data-ttu-id="66639-111">Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado, usando um qualificador ValueMap no método.</span><span class="sxs-lookup"><span data-stu-id="66639-111">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="66639-112">As cadeias de caracteres para as quais o conteúdo de ValueMap são ' convertidas ' também podem ser especificadas na subclasse como um qualificador de matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="66639-112">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="66639-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66639-113">Syntax</span></span>


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="66639-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66639-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66639-115">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66639-115">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66639-116">Se verdadeiro, habilite o dispositivo, se FALSE desabilitar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66639-116">If TRUE enable the device, if FALSE disable the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66639-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66639-117">Return value</span></span>

<span data-ttu-id="66639-118">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="66639-118">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="66639-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66639-119">Requirements</span></span>



| <span data-ttu-id="66639-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="66639-120">Requirement</span></span> | <span data-ttu-id="66639-121">Valor</span><span class="sxs-lookup"><span data-stu-id="66639-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66639-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66639-122">Minimum supported client</span></span><br/> | <span data-ttu-id="66639-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="66639-123">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="66639-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66639-124">Minimum supported server</span></span><br/> | <span data-ttu-id="66639-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="66639-125">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="66639-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="66639-126">Namespace</span></span><br/>                | <span data-ttu-id="66639-127">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="66639-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="66639-128">MOF</span><span class="sxs-lookup"><span data-stu-id="66639-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66639-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66639-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66639-130">DLL</span><span class="sxs-lookup"><span data-stu-id="66639-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66639-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66639-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="66639-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="66639-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66639-133">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="66639-133">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




