---
title: Método INapComponentConfig2 InvokeUIForMachine (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) conforme necessário para gerenciar a configuração remota diretamente no computador especificado. Esse método inicia uma interface do usuário de gerenciamento de configuração.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Método InvokeUIForMachine NAP
- Método InvokeUIForMachine NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, método InvokeUIForMachine
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085493"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a><span data-ttu-id="3513a-107">Método INapComponentConfig2:: InvokeUIForMachine</span><span class="sxs-lookup"><span data-stu-id="3513a-107">INapComponentConfig2::InvokeUIForMachine method</span></span>

> [!Note]  
> <span data-ttu-id="3513a-108">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="3513a-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3513a-109">O método **InvokeUIForMachine** é implementado por SHVs (validadores da integridade do sistema) conforme necessário para gerenciar a configuração remota diretamente no computador especificado.</span><span class="sxs-lookup"><span data-stu-id="3513a-109">The **InvokeUIForMachine** method is implemented by system health validators (SHVs) as needed to manage remote configuration directly on the machine specified.</span></span> <span data-ttu-id="3513a-110">Esse método inicia uma interface do usuário de gerenciamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="3513a-110">This method launches a configuration management UI.</span></span>

## <a name="syntax"></a><span data-ttu-id="3513a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3513a-111">Syntax</span></span>


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a><span data-ttu-id="3513a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3513a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3513a-113">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3513a-113">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3513a-114">Um identificador para a janela pai ou proprietário.</span><span class="sxs-lookup"><span data-stu-id="3513a-114">A handle to the parent or owner window.</span></span> <span data-ttu-id="3513a-115">Um identificador de janela válido deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="3513a-115">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="3513a-116">*MachineName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3513a-116">*machineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3513a-117">Um ponteiro para um [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém o nome do computador do cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="3513a-117">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3513a-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3513a-118">Return value</span></span>

<span data-ttu-id="3513a-119">Retorna S \_ OK se for bem-sucedido ou um dos códigos de erro padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="3513a-119">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3513a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3513a-120">Requirements</span></span>



| <span data-ttu-id="3513a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3513a-121">Requirement</span></span> | <span data-ttu-id="3513a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3513a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3513a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3513a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3513a-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3513a-124">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3513a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3513a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3513a-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3513a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3513a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3513a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3513a-128"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3513a-128"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="3513a-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="3513a-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3513a-130"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3513a-130"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3513a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3513a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3513a-132">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="3513a-132">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





