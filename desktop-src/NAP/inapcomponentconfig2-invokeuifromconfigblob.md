---
title: Método INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon. h)
description: É implementado por SHVs (validadores de integridade do sistema) conforme necessário para carregar a configuração de um computador remoto ou local na memória e exibir uma interface do usuário que permite a manipulação dos dados de configuração.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Método InvokeUIFromConfigBlob NAP
- Método InvokeUIFromConfigBlob NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, método InvokeUIFromConfigBlob
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824291"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a><span data-ttu-id="34360-106">Método INapComponentConfig2:: InvokeUIFromConfigBlob</span><span class="sxs-lookup"><span data-stu-id="34360-106">INapComponentConfig2::InvokeUIFromConfigBlob method</span></span>

> [!Note]  
> <span data-ttu-id="34360-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="34360-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="34360-108">O método **InvokeUIFromConfigBlob** é implementado por SHVs (validadores da integridade do sistema) conforme necessário para carregar a configuração de um computador remoto ou local na memória e exibir uma interface do usuário que permite a manipulação dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="34360-108">The **InvokeUIFromConfigBlob** method is implemented by system health validators (SHVs) as needed to load the configuration of a remote or local machine in memory and display a UI that allows manipulation of the configuration data.</span></span> <span data-ttu-id="34360-109">O componente de configuração deve dar suporte ao uso de [**INapComponentConfig**](inapcomponentconfig.md) por meio do DCOM.</span><span class="sxs-lookup"><span data-stu-id="34360-109">The configuration component must support the usage of [**INapComponentConfig**](inapcomponentconfig.md) through DCOM.</span></span>

## <a name="syntax"></a><span data-ttu-id="34360-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34360-110">Syntax</span></span>


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a><span data-ttu-id="34360-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34360-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34360-112">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34360-112">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34360-113">Um identificador para a janela pai ou proprietário.</span><span class="sxs-lookup"><span data-stu-id="34360-113">A handle to the parent or owner window.</span></span> <span data-ttu-id="34360-114">Um identificador de janela válido deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="34360-114">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="34360-115">*inbCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34360-115">*inbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34360-116">O tamanho, em bytes, dos *indados*.</span><span class="sxs-lookup"><span data-stu-id="34360-116">The size, in bytes, of *inData*.</span></span>

</dd> <dt>

<span data-ttu-id="34360-117">*Indados* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34360-117">*inData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34360-118">Um ponteiro para um buffer que armazena os dados de configuração iniciais.</span><span class="sxs-lookup"><span data-stu-id="34360-118">A pointer to a buffer that stores the initial configuration data.</span></span> <span data-ttu-id="34360-119">Esses dados são exportados do computador remoto ou local.</span><span class="sxs-lookup"><span data-stu-id="34360-119">This data is exported from the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="34360-120">*outbCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="34360-120">*outbCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34360-121">O tamanho, em bytes, dos *OutData*.</span><span class="sxs-lookup"><span data-stu-id="34360-121">The size, in bytes, of *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="34360-122">*OutData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="34360-122">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34360-123">Um ponteiro para um buffer que armazena os dados de configuração alterados pela interface de usuário da configuração do SHV.</span><span class="sxs-lookup"><span data-stu-id="34360-123">A pointer to a buffer that stores configuration data changed by the SHV configuration user interface.</span></span> <span data-ttu-id="34360-124">Esses dados são importados pelo computador remoto ou local.</span><span class="sxs-lookup"><span data-stu-id="34360-124">This data is imported by the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="34360-125">*fConfigChanged* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="34360-125">*fConfigChanged* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34360-126">Um ponteiro para um **bool** que é definido como **true** se a configuração foi alterada durante a operação da interface do usuário; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="34360-126">A pointer to a **BOOL** that is set to **TRUE** if the configuration was changed during the UI operation and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34360-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34360-127">Return value</span></span>

<span data-ttu-id="34360-128">Retorna S \_ OK se for bem-sucedido ou um dos códigos de erro padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="34360-128">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="34360-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="34360-129">Remarks</span></span>

<span data-ttu-id="34360-130">Se usado para um computador local, essa função pode ser usada para a configuração de SHV por política.</span><span class="sxs-lookup"><span data-stu-id="34360-130">If used for a local machine, this function can be used for per policy SHV configuration.</span></span> <span data-ttu-id="34360-131">Ele fornece uma maneira de invocar uma interface do usuário do SHV e editar uma configuração de SHV existente.</span><span class="sxs-lookup"><span data-stu-id="34360-131">It provides a way to invoke an SHV UI and edit an existing SHV configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="34360-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34360-132">Requirements</span></span>



| <span data-ttu-id="34360-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="34360-133">Requirement</span></span> | <span data-ttu-id="34360-134">Valor</span><span class="sxs-lookup"><span data-stu-id="34360-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="34360-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34360-135">Minimum supported client</span></span><br/> | <span data-ttu-id="34360-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="34360-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="34360-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34360-137">Minimum supported server</span></span><br/> | <span data-ttu-id="34360-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34360-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34360-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34360-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="34360-140"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="34360-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="34360-141">INSERI</span><span class="sxs-lookup"><span data-stu-id="34360-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34360-142"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="34360-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34360-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="34360-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34360-144">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="34360-144">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





