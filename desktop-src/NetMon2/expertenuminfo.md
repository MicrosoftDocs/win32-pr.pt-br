---
description: A estrutura EXPERTENUMINFO fornece informações sobre o especialista.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Estrutura EXPERTENUMINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783259"
---
# <a name="expertenuminfo-structure"></a><span data-ttu-id="a5538-103">Estrutura EXPERTENUMINFO</span><span class="sxs-lookup"><span data-stu-id="a5538-103">EXPERTENUMINFO structure</span></span>

<span data-ttu-id="a5538-104">A estrutura **EXPERTENUMINFO** fornece informações sobre o especialista.</span><span class="sxs-lookup"><span data-stu-id="a5538-104">The **EXPERTENUMINFO** structure provides information about the expert.</span></span> <span data-ttu-id="a5538-105">Monitor de Rede aloca memória para a estrutura e a transmite para o especialista ao chamar a função de especialista de [**registro**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="a5538-105">Network Monitor allocates memory for the structure, and passes it to the expert when it calls the [**Register Expert**](register-expert.md) function.</span></span> <span data-ttu-id="a5538-106">Quando o especialista recebe a estrutura, ele deve preencher todas as informações que Monitor de Rede solicitações.</span><span class="sxs-lookup"><span data-stu-id="a5538-106">When the expert receives the structure, it must then fill-in all the information that Network Monitor requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5538-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5538-107">Syntax</span></span>


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a><span data-ttu-id="a5538-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a5538-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5538-109">**szName**</span><span class="sxs-lookup"><span data-stu-id="a5538-109">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-110">Nome do especialista.</span><span class="sxs-lookup"><span data-stu-id="a5538-110">Name of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-111">**szVendor**</span><span class="sxs-lookup"><span data-stu-id="a5538-111">**szVendor**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-112">Nome do fornecedor que cria o especialista.</span><span class="sxs-lookup"><span data-stu-id="a5538-112">Name of the vendor that creates the expert.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-113">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="a5538-113">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-114">Descrição do especialista.</span><span class="sxs-lookup"><span data-stu-id="a5538-114">Description of the expert.</span></span> <span data-ttu-id="a5538-115">O valor do membro **szDescription** pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a5538-115">The value of the **szDescription** member may be **NULL**.</span></span> <span data-ttu-id="a5538-116">Se o nome for muito longo, ele será truncado na configuração do visualizador padrão.</span><span class="sxs-lookup"><span data-stu-id="a5538-116">If the name is too long, it is truncated in the default viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-117">**Versão**</span><span class="sxs-lookup"><span data-stu-id="a5538-117">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-118">O valor deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a5538-118">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-119">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="a5538-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-120">Os sinalizadores a seguir descrevem o especialista.</span><span class="sxs-lookup"><span data-stu-id="a5538-120">The following flags describe the expert.</span></span>



| <span data-ttu-id="a5538-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a5538-121">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="a5538-122">Significado</span><span class="sxs-lookup"><span data-stu-id="a5538-122">Meaning</span></span>                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <span data-ttu-id="a5538-123"><dt>**sinalizador de enumeração de especialista \_ \_ \_ configurável**</dt></span><span class="sxs-lookup"><span data-stu-id="a5538-123"><dt>**EXPERT\_ENUM\_FLAG\_CONFIGURABLE**</dt></span></span> </dl>                                          | <span data-ttu-id="a5538-124">O especialista dá suporte a chamadas para o método [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="a5538-124">The expert supports calls to the [**Configure**](configure.md) method.</span></span> <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <span data-ttu-id="a5538-125"><dt>**Visualizador de sinalizador de enumeração de especialista \_ \_ \_ \_ privado**</dt></span><span class="sxs-lookup"><span data-stu-id="a5538-125"><dt>**EXPERT\_ENUM\_FLAG\_VIEWER\_PRIVATE**</dt></span></span> </dl>                                   | <span data-ttu-id="a5538-126">O especialista requer um Visualizador de Eventos privado (não compartilhado).</span><span class="sxs-lookup"><span data-stu-id="a5538-126">The expert requires a private (non-shared) Event Viewer.</span></span> <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <span data-ttu-id="a5538-127"><dt>**sinalizador de enumeração de especialistas \_ \_ \_ sem \_ Visualizador**</dt></span><span class="sxs-lookup"><span data-stu-id="a5538-127"><dt>**EXPERT\_ENUM\_FLAG\_NO\_VIEWER**</dt></span></span> </dl>                                                  | <span data-ttu-id="a5538-128">O especialista não envia notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="a5538-128">The expert does not send event notifications.</span></span> <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <span data-ttu-id="a5538-129"><dt>**\_ \_ sinalizador de enumeração \_ de especialistas adicionar \_ -me \_ ao \_ RMC \_ no \_ Resumo**</dt></span><span class="sxs-lookup"><span data-stu-id="a5538-129"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_SUMMARY**</dt></span></span> </dl> | <span data-ttu-id="a5538-130">Quando o foco está no painel Resumo, o especialista é exibido no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="a5538-130">When the focus is in the summary pane, the expert appears on the context menu.</span></span> <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <span data-ttu-id="a5538-131"><dt>**\_sinalizador de enumeração \_ de especialista \_ \_ me adicionar \_ a \_ RMC \_ em \_ detalhes**</dt></span><span class="sxs-lookup"><span data-stu-id="a5538-131"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_DETAIL**</dt></span></span> </dl>    | <span data-ttu-id="a5538-132">Quando o foco está no painel de detalhes, o especialista é exibido no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="a5538-132">When the focus is in the detail pane, the expert appears on the context menu.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="a5538-133">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="a5538-133">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-134">Lide com o especialista.</span><span class="sxs-lookup"><span data-stu-id="a5538-134">Handle to the expert.</span></span> <span data-ttu-id="a5538-135">Quando a estrutura **EXPERTENUMINFO** é usada para registrar um especialista, o parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="a5538-135">When the **EXPERTENUMINFO** structure is used to register an expert, the parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-136">**szDllName**</span><span class="sxs-lookup"><span data-stu-id="a5538-136">**szDllName**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-137">Membro privado; Não use.</span><span class="sxs-lookup"><span data-stu-id="a5538-137">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-138">**hModule**</span><span class="sxs-lookup"><span data-stu-id="a5538-138">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-139">Membro privado; Não use.</span><span class="sxs-lookup"><span data-stu-id="a5538-139">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-140">**pRegisterProc**</span><span class="sxs-lookup"><span data-stu-id="a5538-140">**pRegisterProc**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-141">Membro privado; Não use.</span><span class="sxs-lookup"><span data-stu-id="a5538-141">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-142">**pConfigProc**</span><span class="sxs-lookup"><span data-stu-id="a5538-142">**pConfigProc**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-143">Membro privado; Não use.</span><span class="sxs-lookup"><span data-stu-id="a5538-143">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="a5538-144">**pRunProc**</span><span class="sxs-lookup"><span data-stu-id="a5538-144">**pRunProc**</span></span>
</dt> <dd>

<span data-ttu-id="a5538-145">Membro privado; Não use.</span><span class="sxs-lookup"><span data-stu-id="a5538-145">Private member; do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5538-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5538-146">Requirements</span></span>



| <span data-ttu-id="a5538-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5538-147">Requirement</span></span> | <span data-ttu-id="a5538-148">Valor</span><span class="sxs-lookup"><span data-stu-id="a5538-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a5538-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5538-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a5538-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a5538-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a5538-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5538-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a5538-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a5538-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a5538-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a5538-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5538-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5538-154"><dt>Netmon.h</dt></span></span> </dl> |



 

 




