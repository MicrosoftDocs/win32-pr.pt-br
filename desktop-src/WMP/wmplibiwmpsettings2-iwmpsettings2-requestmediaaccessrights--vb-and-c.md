---
title: Método IWMPSettings2 requestMediaAccessRights
description: O método requestMediaAccessRights solicita um nível especificado de acesso à biblioteca. | Método IWMPSettings2 requestMediaAccessRights
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- método requestMediaAccessRights Windows Media Player
- método requestMediaAccessRights Windows Media Player, interface IWMPSettings2
- Interface IWMPSettings2 Windows Media Player, método requestMediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761315"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a><span data-ttu-id="c176d-107">Método IWMPSettings2:: requestMediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="c176d-107">IWMPSettings2::requestMediaAccessRights method</span></span>

<span data-ttu-id="c176d-108">O método **requestMediaAccessRights** solicita um nível especificado de acesso à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c176d-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c176d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c176d-109">Syntax</span></span>


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a><span data-ttu-id="c176d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c176d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c176d-111">*bstrDesiredAccess* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c176d-111">*bstrDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c176d-112">Um **System. String** que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c176d-112">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="c176d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c176d-113">Value</span></span> | <span data-ttu-id="c176d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c176d-114">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="c176d-115">none</span><span class="sxs-lookup"><span data-stu-id="c176d-115">none</span></span>  | <span data-ttu-id="c176d-116">Somente direitos de acesso do item atual.</span><span class="sxs-lookup"><span data-stu-id="c176d-116">Current item access rights only.</span></span> |
| <span data-ttu-id="c176d-117">ler</span><span class="sxs-lookup"><span data-stu-id="c176d-117">read</span></span>  | <span data-ttu-id="c176d-118">Somente direitos de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="c176d-118">Read access rights only.</span></span>         |
| <span data-ttu-id="c176d-119">completa</span><span class="sxs-lookup"><span data-stu-id="c176d-119">full</span></span>  | <span data-ttu-id="c176d-120">Direitos de acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c176d-120">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c176d-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c176d-121">Return value</span></span>

<span data-ttu-id="c176d-122">Um **System. Boolean** que indica se os direitos de acesso solicitados foram concedidos.</span><span class="sxs-lookup"><span data-stu-id="c176d-122">A **System.Boolean** that indicates whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="c176d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c176d-123">Remarks</span></span>

<span data-ttu-id="c176d-124">Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c176d-124">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="c176d-125">Invocar esse método solicita ao usuário uma caixa de diálogo que solicita o nível de permissão especificado.</span><span class="sxs-lookup"><span data-stu-id="c176d-125">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="c176d-126">Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos.</span><span class="sxs-lookup"><span data-stu-id="c176d-126">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="c176d-127">O nível de direitos de acesso atual pode ser recuperado usando **IWMPSettings2. mediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="c176d-127">The current access rights level can be retrieved by using **IWMPSettings2.mediaAccessRights**.</span></span>

<span data-ttu-id="c176d-128">Os aplicativos em execução no computador do usuário não são obrigados a usar esse método.</span><span class="sxs-lookup"><span data-stu-id="c176d-128">Applications running on the user's computer are not required to use this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c176d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c176d-129">Requirements</span></span>



| <span data-ttu-id="c176d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c176d-130">Requirement</span></span> | <span data-ttu-id="c176d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c176d-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c176d-132">Versão</span><span class="sxs-lookup"><span data-stu-id="c176d-132">Version</span></span><br/>   | <span data-ttu-id="c176d-133">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c176d-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c176d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="c176d-134">Namespace</span></span><br/> | <span data-ttu-id="c176d-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c176d-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c176d-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="c176d-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c176d-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c176d-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c176d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c176d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c176d-139">**Interface IWMPSettings2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c176d-139">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c176d-140">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c176d-140">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





