---
description: Usado com a \_ propriedade de propriedade de política de IU NCRYPT \_ \_ para conter informações de interface de usuário para uma chave.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Estrutura de NCRYPT_UI_POLICY_BLOB ( \_ provedor de NCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505752"
---
# <a name="ncrypt_ui_policy_blob-structure"></a><span data-ttu-id="31062-103">\_Estrutura de \_ blob de política de IU NCRYPT \_</span><span class="sxs-lookup"><span data-stu-id="31062-103">NCRYPT\_UI\_POLICY\_BLOB structure</span></span>

<span data-ttu-id="31062-104">A estrutura de **\_ blob de \_ política \_ de interface do usuário NCrypt** é usada com a propriedade de [**\_ propriedade de \_ diretiva \_ NCrypt UI**](key-storage-property-identifiers.md) para conter informações de interface de usuário para uma chave.</span><span class="sxs-lookup"><span data-stu-id="31062-104">The **NCRYPT\_UI\_POLICY\_BLOB** structure is used with the [**NCRYPT\_UI\_POLICY\_PROPERTY**](key-storage-property-identifiers.md) property to contain user interface information for a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="31062-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31062-105">Syntax</span></span>


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a><span data-ttu-id="31062-106">Membros</span><span class="sxs-lookup"><span data-stu-id="31062-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="31062-107">**DW**</span><span class="sxs-lookup"><span data-stu-id="31062-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="31062-108">O número de versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="31062-108">The version number of the structure.</span></span> <span data-ttu-id="31062-109">Este membro deve conter 1.</span><span class="sxs-lookup"><span data-stu-id="31062-109">This member must contain 1.</span></span>

</dd> <dt>

<span data-ttu-id="31062-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="31062-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="31062-111">Um conjunto de sinalizadores que fornecem informações ou requisitos adicionais da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="31062-111">A set of flags that provide additional user interface information or requirements.</span></span>



| <span data-ttu-id="31062-112">Valor</span><span class="sxs-lookup"><span data-stu-id="31062-112">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="31062-113">Significado</span><span class="sxs-lookup"><span data-stu-id="31062-113">Meaning</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <span data-ttu-id="31062-114"><dt>**NCRYPT \_ \_Sinalizador de \_ chave \_ de proteção de interface de usuário**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="31062-114"><dt>**NCRYPT\_UI\_PROTECT\_KEY\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="31062-115">Exiba a interface do usuário de chave forte, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="31062-115">Display the strong key user interface as needed.</span></span><br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <span data-ttu-id="31062-116"><dt>**NCRYPT \_ \_Sinalizador de \_ alta \_ proteção \_ da força de interface do usuário**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="31062-116"><dt>**NCRYPT\_UI\_FORCE\_HIGH\_PROTECTION\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="31062-117">Force alta proteção.</span><span class="sxs-lookup"><span data-stu-id="31062-117">Force high protection.</span></span><br/>                           |



 

</dd> <dt>

<span data-ttu-id="31062-118">**cbCreationTitle**</span><span class="sxs-lookup"><span data-stu-id="31062-118">**cbCreationTitle**</span></span>
</dt> <dd>

<span data-ttu-id="31062-119">O comprimento, em bytes, do título de criação.</span><span class="sxs-lookup"><span data-stu-id="31062-119">The length, in bytes, of the creation title.</span></span> <span data-ttu-id="31062-120">O título de criação é uma cadeia de caracteres Unicode terminada em nulo que especifica o texto que é usado como o título da caixa de diálogo de chave forte quando a chave é concluída.</span><span class="sxs-lookup"><span data-stu-id="31062-120">The creation title is a null-terminated Unicode string that specifies the text that is used as the title of the strong key dialog box when the key is completed.</span></span> <span data-ttu-id="31062-121">O título de criação deve ser colocado imediatamente após a estrutura de **\_ BLOB da \_ diretiva \_ de interface do usuário NCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="31062-121">The creation title must be placed immediately following the **NCRYPT\_UI\_POLICY\_BLOB** structure.</span></span> <span data-ttu-id="31062-122">Se o valor do membro **cbCreationTitle** for definido como 0, um título de criação padrão será usado para o título da caixa de diálogo de chave forte.</span><span class="sxs-lookup"><span data-stu-id="31062-122">If the value of the **cbCreationTitle** member is set to 0, a default creation title is used for the title of the strong key dialog box.</span></span> <span data-ttu-id="31062-123">Esse membro só é usado na finalização de chave.</span><span class="sxs-lookup"><span data-stu-id="31062-123">This member is only used on key finalization.</span></span>

</dd> <dt>

<span data-ttu-id="31062-124">**cbFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="31062-124">**cbFriendlyName**</span></span>
</dt> <dd>

<span data-ttu-id="31062-125">O comprimento, em bytes, do nome amigável da chave.</span><span class="sxs-lookup"><span data-stu-id="31062-125">The length, in bytes, of the friendly name of the key.</span></span> <span data-ttu-id="31062-126">O nome amigável é uma cadeia de caracteres Unicode terminada em nulo que contém o texto que é exibido na caixa de diálogo chave forte como o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="31062-126">The friendly name is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the name of the key.</span></span> <span data-ttu-id="31062-127">O nome amigável deve ser colocado imediatamente após o título de criação neste BLOB.</span><span class="sxs-lookup"><span data-stu-id="31062-127">The friendly name must be placed immediately following the creation title in this BLOB.</span></span> <span data-ttu-id="31062-128">Se o valor do membro **cbFriendlyName** for definido como 0, um nome padrão será usado na caixa de diálogo chave forte.</span><span class="sxs-lookup"><span data-stu-id="31062-128">If the value of the **cbFriendlyName** member is set to 0, a default name is used in the strong key dialog box.</span></span> <span data-ttu-id="31062-129">Esse membro é usado quando a chave é concluída e quando a chave é usada.</span><span class="sxs-lookup"><span data-stu-id="31062-129">This member is used both when the key is completed and when the key is used.</span></span>

</dd> <dt>

<span data-ttu-id="31062-130">**cbDescription**</span><span class="sxs-lookup"><span data-stu-id="31062-130">**cbDescription**</span></span>
</dt> <dd>

<span data-ttu-id="31062-131">O comprimento, em bytes, da descrição da chave.</span><span class="sxs-lookup"><span data-stu-id="31062-131">The length, in bytes, of the key description.</span></span> <span data-ttu-id="31062-132">A descrição da chave é uma cadeia de caracteres Unicode terminada em nulo que contém o texto que é exibido na caixa de diálogo chave forte como a descrição da chave.</span><span class="sxs-lookup"><span data-stu-id="31062-132">The key description is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the description of the key.</span></span> <span data-ttu-id="31062-133">O valor da descrição deve ser colocado imediatamente após o nome amigável neste BLOB.</span><span class="sxs-lookup"><span data-stu-id="31062-133">The description value must be placed immediately following the friendly name in this BLOB.</span></span> <span data-ttu-id="31062-134">Se o valor do membro **cbDescription** for definido como 0, uma descrição padrão será usada na caixa de diálogo chave forte.</span><span class="sxs-lookup"><span data-stu-id="31062-134">If the value of the **cbDescription** member is set to 0, a default description is used in the strong key dialog box.</span></span> <span data-ttu-id="31062-135">Esse membro é usado quando a chave é concluída e quando a chave é usada.</span><span class="sxs-lookup"><span data-stu-id="31062-135">This member is used both when the key is completed and when the key is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31062-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="31062-136">Remarks</span></span>

<span data-ttu-id="31062-137">Essa estrutura está incluída no cabeçalho NCrypt \_ Provider. h.</span><span class="sxs-lookup"><span data-stu-id="31062-137">This structure is included in the Ncrypt\_provider.h header.</span></span> <span data-ttu-id="31062-138">Para usar a estrutura, você deve baixar o [Kit de desenvolvimento do provedor criptográfico](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) do Microsoft Connect.</span><span class="sxs-lookup"><span data-stu-id="31062-138">To use the structure, you must download the [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) from Microsoft Connect.</span></span>

## <a name="requirements"></a><span data-ttu-id="31062-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31062-139">Requirements</span></span>



| <span data-ttu-id="31062-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="31062-140">Requirement</span></span> | <span data-ttu-id="31062-141">Valor</span><span class="sxs-lookup"><span data-stu-id="31062-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31062-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31062-142">Minimum supported client</span></span><br/> | <span data-ttu-id="31062-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31062-143">Windows Vista \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="31062-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31062-144">Minimum supported server</span></span><br/> | <span data-ttu-id="31062-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31062-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="31062-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31062-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="31062-147"><dt>NCrypt \_ Provider. h</dt></span><span class="sxs-lookup"><span data-stu-id="31062-147"><dt>Ncrypt\_provider.h</dt></span></span> </dl> |



 

