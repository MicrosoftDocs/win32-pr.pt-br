---
description: O \_ tipo de enumeração excluir opções de objeto \_ descreve as opções que têm suporte de um dispositivo ao excluir um objeto.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Enumeração de DELETE_OBJECT_OPTIONS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763057"
---
# <a name="delete_object_options-enumeration"></a><span data-ttu-id="28e91-103">Enumeração de opções de excluir \_ objeto \_</span><span class="sxs-lookup"><span data-stu-id="28e91-103">DELETE\_OBJECT\_OPTIONS enumeration</span></span>

<span data-ttu-id="28e91-104">O tipo de enumeração **excluir \_ \_ Opções de objeto** descreve as opções que têm suporte de um dispositivo ao excluir um objeto.</span><span class="sxs-lookup"><span data-stu-id="28e91-104">The **DELETE\_OBJECT\_OPTIONS** enumeration type describes options that are supported by a device when deleting an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e91-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28e91-105">Syntax</span></span>


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="28e91-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="28e91-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="28e91-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**\_exclusão de dispositivo portátil \_ \_ sem \_ recursão**</span><span class="sxs-lookup"><span data-stu-id="28e91-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_NO\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="28e91-108">Exclua apenas o objeto e falhe se ele tiver filhos.</span><span class="sxs-lookup"><span data-stu-id="28e91-108">Delete the object only and fail if it has children.</span></span>

</dd> <dt>

<span data-ttu-id="28e91-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_ \_ exclusão de dispositivo portátil \_ com \_ recursão**</span><span class="sxs-lookup"><span data-stu-id="28e91-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_WITH\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="28e91-110">Exclua o objeto e todos os seus filhos.</span><span class="sxs-lookup"><span data-stu-id="28e91-110">Delete the object and all its children.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28e91-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="28e91-111">Remarks</span></span>

<span data-ttu-id="28e91-112">O aplicativo pode recuperar as opções de exclusão que o dispositivo suporta chamando [**IPortableDeviceCapabilities:: Getcommandoptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) para o comando de **\_ \_ \_ \_ excluir \_ objetos do gerenciamento** de objetos de comando WPD.</span><span class="sxs-lookup"><span data-stu-id="28e91-112">The application can retrieve the deletion options that the device supports by calling [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) for the **WPD\_COMMAND\_OBJECT\_MANAGEMENT\_DELETE\_OBJECTS** command.</span></span> <span data-ttu-id="28e91-113">Ele deve examinar o valor de opção de **\_ \_ \_ exclusão recursiva do objeto de opção WPD \_ \_ \_ com suporte** que esse método retorna em um objeto [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) .</span><span class="sxs-lookup"><span data-stu-id="28e91-113">It should examine the **WPD\_OPTION\_OBJECT\_MANAGEMENT\_RECURSIVE\_DELETE\_SUPPORTED** option value that this method returns in an [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e91-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28e91-114">Requirements</span></span>



| <span data-ttu-id="28e91-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e91-115">Requirement</span></span> | <span data-ttu-id="28e91-116">Valor</span><span class="sxs-lookup"><span data-stu-id="28e91-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e91-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28e91-117">Header</span></span><br/> | <dl> <span data-ttu-id="28e91-118"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="28e91-118"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e91-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="28e91-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e91-120">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="28e91-120">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




