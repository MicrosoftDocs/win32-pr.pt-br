---
title: Classe MDM_Personalization
description: A classe de personalização de MDM \_ é usada para definir as imagens da tela de bloqueio e do plano de fundo da área de trabalho. A definição dessas políticas também impede que o usuário altere a imagem.
ms.assetid: 99b60767-b321-4ec6-9802-76221d26c830
keywords:
- Classe MDM_Personalization
- Classe MDM_Personalization, descrita
topic_type:
- apiref
api_name:
- MDM_Personalization
- MDM_Personalization.InstanceID
- MDM_Personalization.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78986422cce15d750e1ae678aef352bbb369bfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918254"
---
# <a name="mdm_personalization-class"></a><span data-ttu-id="02ccc-106">Classe de personalização de MDM \_</span><span class="sxs-lookup"><span data-stu-id="02ccc-106">MDM\_Personalization class</span></span>

<span data-ttu-id="02ccc-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="02ccc-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="02ccc-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="02ccc-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="02ccc-109">A classe de personalização de MDM \_ é usada para definir as imagens da tela de bloqueio e do plano de fundo da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="02ccc-109">The MDM\_Personalization class is used to set the lock screen and desktop background images.</span></span> <span data-ttu-id="02ccc-110">A definição dessas políticas também impede que o usuário altere a imagem.</span><span class="sxs-lookup"><span data-stu-id="02ccc-110">Setting these policies also prevents the user from changing the image.</span></span>

<span data-ttu-id="02ccc-111">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="02ccc-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ccc-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02ccc-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Personalization
{
  string InstanceID;
  string ParentID;
  string DesktopImageUrl;
  sint32 DesktopImageStatus;
  string LockScreenImageUrl;
  sint32 LockScreenImageStatus;
};
```

## <a name="members"></a><span data-ttu-id="02ccc-113">Membros</span><span class="sxs-lookup"><span data-stu-id="02ccc-113">Members</span></span>

<span data-ttu-id="02ccc-114">A classe de **\_ personalização de MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="02ccc-114">The **MDM\_Personalization** class has these types of members:</span></span>

-   [<span data-ttu-id="02ccc-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02ccc-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02ccc-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02ccc-116">Properties</span></span>

<span data-ttu-id="02ccc-117">A classe de **\_ personalização de MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="02ccc-117">The **MDM\_Personalization** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="02ccc-118">DesktopImageStatus</span><span class="sxs-lookup"><span data-stu-id="02ccc-118">DesktopImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#desktopimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ccc-119">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02ccc-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02ccc-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="02ccc-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02ccc-121">DesktopImageUrl</span><span class="sxs-lookup"><span data-stu-id="02ccc-121">DesktopImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#desktopimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ccc-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="02ccc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02ccc-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="02ccc-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="02ccc-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="02ccc-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ccc-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="02ccc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02ccc-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02ccc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ccc-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02ccc-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02ccc-128">LockScreenImageStatus</span><span class="sxs-lookup"><span data-stu-id="02ccc-128">LockScreenImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ccc-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02ccc-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02ccc-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="02ccc-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02ccc-131">LockScreenImageUrl</span><span class="sxs-lookup"><span data-stu-id="02ccc-131">LockScreenImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ccc-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="02ccc-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02ccc-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="02ccc-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="02ccc-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="02ccc-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ccc-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="02ccc-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02ccc-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02ccc-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ccc-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02ccc-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02ccc-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02ccc-138">Requirements</span></span>



| <span data-ttu-id="02ccc-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="02ccc-139">Requirement</span></span> | <span data-ttu-id="02ccc-140">Valor</span><span class="sxs-lookup"><span data-stu-id="02ccc-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02ccc-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02ccc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="02ccc-142">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="02ccc-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="02ccc-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02ccc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="02ccc-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="02ccc-144">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="02ccc-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="02ccc-145">Namespace</span></span><br/>                | <span data-ttu-id="02ccc-146">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="02ccc-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="02ccc-147">MOF</span><span class="sxs-lookup"><span data-stu-id="02ccc-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02ccc-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02ccc-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="02ccc-149">DLL</span><span class="sxs-lookup"><span data-stu-id="02ccc-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02ccc-150"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02ccc-150"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

