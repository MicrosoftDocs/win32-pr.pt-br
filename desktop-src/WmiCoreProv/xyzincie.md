---
description: Contém as coordenadas da exibição no espaço de cores da CIE (Comissão Internacional de iluminação) XYZ.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Classe XYZinCIE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798019"
---
# <a name="xyzincie-class"></a><span data-ttu-id="9b830-103">Classe XYZinCIE</span><span class="sxs-lookup"><span data-stu-id="9b830-103">XYZinCIE class</span></span>

<span data-ttu-id="9b830-104">A classe WMI **XYZinCIE** contém as coordenadas da exibição no espaço de cores da CIE (Comissão Internacional em iluminação) XYZ.</span><span class="sxs-lookup"><span data-stu-id="9b830-104">The **XYZinCIE** WMI class contains the coordinates of the display in the International Commission on Illumination (CIE) XYZ color space.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b830-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b830-105">Syntax</span></span>

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a><span data-ttu-id="9b830-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9b830-106">Members</span></span>

<span data-ttu-id="9b830-107">A classe **XYZinCIE** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9b830-107">The **XYZinCIE** class has these types of members:</span></span>

-   [<span data-ttu-id="9b830-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9b830-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b830-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9b830-109">Properties</span></span>

<span data-ttu-id="9b830-110">A classe **XYZinCIE** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9b830-110">The **XYZinCIE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b830-111">**X**</span><span class="sxs-lookup"><span data-stu-id="9b830-111">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b830-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b830-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b830-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b830-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b830-114">Coordenada X.</span><span class="sxs-lookup"><span data-stu-id="9b830-114">X-coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9b830-115">**S**</span><span class="sxs-lookup"><span data-stu-id="9b830-115">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b830-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b830-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b830-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b830-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b830-118">Coordenada Y.</span><span class="sxs-lookup"><span data-stu-id="9b830-118">Y-coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b830-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b830-119">Remarks</span></span>

<span data-ttu-id="9b830-120">A classe [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contém instâncias incorporadas da classe **XYZinCIE** para descrever as características de cor de um monitor.</span><span class="sxs-lookup"><span data-stu-id="9b830-120">The [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) class contains embedded instances of the **XYZinCIE** class to describe the color characteristics of a monitor.</span></span>

<span data-ttu-id="9b830-121">Para calcular a coordenada z, com base nos valores x e y, use a relação \| \| (x, y, z) \| \| = 1.</span><span class="sxs-lookup"><span data-stu-id="9b830-121">To calculate the z-coordinate, based on the x and y values, use the relation \|\|(x,y,z)\|\| = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b830-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b830-122">Requirements</span></span>



| <span data-ttu-id="9b830-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b830-123">Requirement</span></span> | <span data-ttu-id="9b830-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9b830-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b830-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b830-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9b830-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b830-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9b830-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b830-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9b830-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b830-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9b830-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b830-129">Namespace</span></span><br/>                | <span data-ttu-id="9b830-130">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="9b830-130">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9b830-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9b830-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b830-132"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b830-132"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b830-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9b830-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b830-134"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b830-134"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b830-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b830-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b830-136">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="9b830-136">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




