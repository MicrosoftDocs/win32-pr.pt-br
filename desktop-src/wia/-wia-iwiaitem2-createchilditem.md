---
description: Crie um novo item filho. Adiciona objetos IWiaItem2 à árvore IWiaItem2 do dispositivo.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'Método IWiaItem2:: createchilditem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808231"
---
# <a name="iwiaitem2createchilditem-method"></a><span data-ttu-id="e212b-104">Método IWiaItem2:: createchilditem</span><span class="sxs-lookup"><span data-stu-id="e212b-104">IWiaItem2::CreateChildItem method</span></span>

<span data-ttu-id="e212b-105">Crie um novo item filho.</span><span class="sxs-lookup"><span data-stu-id="e212b-105">Create a new child item.</span></span> <span data-ttu-id="e212b-106">Adiciona objetos [**IWiaItem2**](-wia-iwiaitem2.md) à árvore **IWiaItem2** do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e212b-106">Adds [**IWiaItem2**](-wia-iwiaitem2.md) objects to a device's **IWiaItem2** tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="e212b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e212b-107">Syntax</span></span>


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="e212b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e212b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e212b-109">*lItemFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e212b-109">*lItemFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e212b-110">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="e212b-110">Type: **LONG**</span></span>

<span data-ttu-id="e212b-111">Especifica o tipo de item WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="e212b-111">Specifies the WIA 2.0 item type.</span></span> <span data-ttu-id="e212b-112">Consulte [**sinalizadores de tipo de item WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e212b-112">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="e212b-113">*lCreationFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e212b-113">*lCreationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e212b-114">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="e212b-114">Type: **LONG**</span></span>

<span data-ttu-id="e212b-115">Especifica como criar o novo item.</span><span class="sxs-lookup"><span data-stu-id="e212b-115">Specifies how to create the new item.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="e212b-116"><span id="0"></span>**0** (0)</span><span class="sxs-lookup"><span data-stu-id="e212b-116"><span id="0"></span>**0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e212b-117">Defina os valores padrão para as propriedades do filho.</span><span class="sxs-lookup"><span data-stu-id="e212b-117">Set the default values for the properties of the child.</span></span>

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span data-ttu-id="e212b-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Copiar \_ \_ \_ Valores de propriedade pai** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="e212b-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY\_PARENT\_PROPERTY\_VALUES** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="e212b-119">Copie os valores de todas as propriedades de leitura/gravação do pai.</span><span class="sxs-lookup"><span data-stu-id="e212b-119">Copy the values of all Read/Write properties from the parent.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e212b-120">*bstrItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e212b-120">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e212b-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e212b-121">Type: **BSTR**</span></span>

<span data-ttu-id="e212b-122">Especifica o nome do item.</span><span class="sxs-lookup"><span data-stu-id="e212b-122">Specifies the item name.</span></span> <span data-ttu-id="e212b-123">Esse nome é acrescentado ao final do nome do item pai para gerar o nome completo do item.</span><span class="sxs-lookup"><span data-stu-id="e212b-123">This name is appended to the end of the parent item's name to generate the full item name.</span></span>

</dd> <dt>

<span data-ttu-id="e212b-124">*ppIWiaItem2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e212b-124">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e212b-125">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e212b-125">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="e212b-126">Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) que define o método **IWiaItem2:: createchilditem** .</span><span class="sxs-lookup"><span data-stu-id="e212b-126">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface that sets the **IWiaItem2::CreateChildItem** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e212b-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e212b-127">Return value</span></span>

<span data-ttu-id="e212b-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e212b-128">Type: **HRESULT**</span></span>

<span data-ttu-id="e212b-129">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e212b-129">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e212b-130">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e212b-130">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e212b-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e212b-131">Remarks</span></span>

<span data-ttu-id="e212b-132">Alguns dispositivos de hardware WIA 2,0 permitem que os aplicativos criem novos itens na árvore [**IWiaItem2**](-wia-iwiaitem2.md) que representa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e212b-132">Some WIA 2.0 hardware devices allow applications to create new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree that represents the device.</span></span> <span data-ttu-id="e212b-133">Os aplicativos devem testar os dispositivos para ver se eles dão suporte a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="e212b-133">Applications must test the devices to see if they support this capability.</span></span> <span data-ttu-id="e212b-134">Use a \_ interface IEnumWIA dev \_ Caps para enumerar os recursos atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e212b-134">Use the IEnumWIA\_DEV\_CAPS interface to enumerate the current device's capabilities.</span></span>

<span data-ttu-id="e212b-135">Se o dispositivo permitir a criação de novos itens na árvore [**IWiaItem2**](-wia-iwiaitem2.md) , invocar **IWiaItem2:: createchilditem** cria um novo objeto **IWiaItem2** que é filho do nó atual.</span><span class="sxs-lookup"><span data-stu-id="e212b-135">If the device allows the creation of new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree, invoking **IWiaItem2::CreateChildItem** creates a new **IWiaItem2** object that is a child of the current node.</span></span> <span data-ttu-id="e212b-136">Ele passa um ponteiro para o novo nó para o aplicativo por meio do parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="e212b-136">It passes a pointer to the new node to the application through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="e212b-137">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="e212b-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="e212b-138">Se *lCreationFlags* for copiar \_ \_ \_ valores de propriedade pai e *lItemFlags* for zero, a função retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="e212b-138">If *lCreationFlags* is COPY\_PARENT\_PROPERTY\_VALUES and *lItemFlags* is zero, the function returns E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="e212b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e212b-139">Requirements</span></span>



| <span data-ttu-id="e212b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e212b-140">Requirement</span></span> | <span data-ttu-id="e212b-141">Valor</span><span class="sxs-lookup"><span data-stu-id="e212b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e212b-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e212b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e212b-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e212b-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e212b-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e212b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e212b-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e212b-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e212b-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e212b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e212b-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e212b-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="e212b-148">INSERI</span><span class="sxs-lookup"><span data-stu-id="e212b-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e212b-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e212b-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
