---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades diversas.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Propriedades diversas (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769140"
---
# <a name="miscellaneous-properties"></a><span data-ttu-id="b0296-103">Propriedades diversas</span><span class="sxs-lookup"><span data-stu-id="b0296-103">Miscellaneous Properties</span></span>

<span data-ttu-id="b0296-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades diversas.</span><span class="sxs-lookup"><span data-stu-id="b0296-104">Windows Portable Devices supports the following miscellaneous properties.</span></span>



| <span data-ttu-id="b0296-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b0296-105">Property</span></span>                                       | <span data-ttu-id="b0296-106">VarType</span><span class="sxs-lookup"><span data-stu-id="b0296-106">VarType</span></span>         | <span data-ttu-id="b0296-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0296-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0296-108">**a \_ opção de API WPD \_ \_ usa \_ fluxo de dados claros \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b0296-108">**WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM**</span></span> | <span data-ttu-id="b0296-109">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="b0296-109">**VT\_BOOL**</span></span>    | <span data-ttu-id="b0296-110">Um valor booliano que especifica se o fluxo de dados criado para transferência de dados será claro, ou seja, o DRM não está envolvido. Os clientes podem definir essa opção adicionando-a às propriedades do objeto passado para [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="b0296-110">A Boolean value that specifies whether the data stream created for data transfer will be clear, that is, DRM is not involved.Clients can set this option by adding it to the object properties passed to [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="b0296-111">**\_versão do serviço WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b0296-111">**WPD\_SERVICE\_VERSION**</span></span>                      | <span data-ttu-id="b0296-112">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="b0296-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="b0296-113">Uma cadeia de caracteres que especifica a versão de implementação de um determinado serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0296-113">A string that specifies the implementation version of a given device service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="b0296-114">**\_tipos de conteúdo de pasta WPD \_ \_ \_ permitidos**</span><span class="sxs-lookup"><span data-stu-id="b0296-114">**WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED**</span></span>       | <span data-ttu-id="b0296-115">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="b0296-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="b0296-116">Um valor que especifica os tipos de objeto que podem ser filhos diretos dessa pasta.</span><span class="sxs-lookup"><span data-stu-id="b0296-116">A value that specifies the object types that can be direct children of this folder.</span></span> <span data-ttu-id="b0296-117">As pastas filhas podem ter recursos diferentes. Essa propriedade é um [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém \_ valores de CLSID VT que especificam tipos de objeto permitidos.</span><span class="sxs-lookup"><span data-stu-id="b0296-117">Child folders can have different capabilities.This property is an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) holding VT\_CLSID values that specify permitted object types.</span></span><br/> <span data-ttu-id="b0296-118">Para obter uma lista de tipos de objeto definidos por dispositivos portáteis do Windows, consulte [requisitos para objetos](requirements-for-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b0296-118">For a list of object types defined by Windows Portable Devices, see [Requirements for Objects](requirements-for-objects.md).</span></span><br/>                                         |
| <span data-ttu-id="b0296-119">**\_categoria de \_ objeto \_ funcional WPD**</span><span class="sxs-lookup"><span data-stu-id="b0296-119">**WPD\_FUNCTIONAL\_OBJECT\_CATEGORY**</span></span>          | <span data-ttu-id="b0296-120">**CLSID do VT \_**</span><span class="sxs-lookup"><span data-stu-id="b0296-120">**VT\_CLSID**</span></span>   | <span data-ttu-id="b0296-121">Um valor que especifica a categoria funcional do objeto.</span><span class="sxs-lookup"><span data-stu-id="b0296-121">A value that specifies the object's functional category.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b0296-122">**\_perfis de \_ informações de renderização WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b0296-122">**WPD\_RENDERING\_INFORMATION\_PROFILES**</span></span>      | <span data-ttu-id="b0296-123">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="b0296-123">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="b0296-124">Um [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) que contém várias interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) , cada uma delas contendo as configurações de propriedade para um perfil ao qual o objeto dá suporte.</span><span class="sxs-lookup"><span data-stu-id="b0296-124">An [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) that holds multiple [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces, each of which contains the property settings for a profile that the object supports.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="b0296-125">**\_nome de \_ exibição do local de dica de objeto WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b0296-125">**WPD\_OBJECT\_HINT\_LOCATION\_DISPLAY\_NAME**</span></span> | <span data-ttu-id="b0296-126">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="b0296-126">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="b0296-127">Se um objeto for um local de dica, essa propriedade indicará o nome específico da dica a ser exibido para o usuário em vez do nome do objeto. Os drivers podem especificar dicas de local para vários tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="b0296-127">If an object is a hint location, this property indicates the hint-specific name to display to the user instead of the object name.Drivers can specify location hints for various object types.</span></span> <span data-ttu-id="b0296-128">Esses são locais de armazenamento preferenciais para pastas que mantêm um tipo de objeto específico.</span><span class="sxs-lookup"><span data-stu-id="b0296-128">These are preferred storage locations for folders that hold a particular object type.</span></span> <span data-ttu-id="b0296-129">Um equivalente seria a pasta minhas imagens para arquivos de imagem no Windows.</span><span class="sxs-lookup"><span data-stu-id="b0296-129">An equivalent would be the My Pictures folder for image files in Windows.</span></span> <span data-ttu-id="b0296-130">Se essa propriedade não existir, normalmente o [nome do \_ objeto \_ WPD](object-properties.md) será usado.</span><span class="sxs-lookup"><span data-stu-id="b0296-130">If this property does not exist, typically the [WPD\_OBJECT\_NAME](object-properties.md) is used instead.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0296-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0296-131">Requirements</span></span>



| <span data-ttu-id="b0296-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0296-132">Requirement</span></span> | <span data-ttu-id="b0296-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b0296-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0296-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0296-134">Header</span></span><br/> | <dl> <span data-ttu-id="b0296-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0296-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0296-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0296-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0296-137">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="b0296-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




