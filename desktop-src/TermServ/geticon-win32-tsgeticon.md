---
title: Método GetIcon da classe Win32_TSGetIcon
description: Retorna o conteúdo do ícone especificado.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Método GetIcon Serviços de Área de Trabalho Remota
- Método GetIcon Serviços de Área de Trabalho Remota, classe Win32_TSGetIcon
- Classe Win32_TSGetIcon Serviços de Área de Trabalho Remota, método GetIcon
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918076"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a><span data-ttu-id="72867-106">Método GetIcon da \_ classe TSGetIcon do Win32</span><span class="sxs-lookup"><span data-stu-id="72867-106">GetIcon method of the Win32\_TSGetIcon class</span></span>

<span data-ttu-id="72867-107">Retorna o conteúdo do ícone especificado.</span><span class="sxs-lookup"><span data-stu-id="72867-107">Returns the contents of the specified icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="72867-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72867-108">Syntax</span></span>


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a><span data-ttu-id="72867-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72867-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72867-110">*FilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72867-110">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72867-111">Especifica o caminho para o arquivo que contém o ícone</span><span class="sxs-lookup"><span data-stu-id="72867-111">Specifies the path to the file that contains the icon</span></span>

</dd> <dt>

<span data-ttu-id="72867-112">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="72867-112">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72867-113">Especifica o índice do ícone no arquivo.</span><span class="sxs-lookup"><span data-stu-id="72867-113">Specifies the index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="72867-114">*IconContents* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="72867-114">*IconContents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72867-115">Em conclusão bem-sucedida, contém o conteúdo do ícone.</span><span class="sxs-lookup"><span data-stu-id="72867-115">On successful completion contains the contents of the icon.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72867-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72867-116">Requirements</span></span>



| <span data-ttu-id="72867-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="72867-117">Requirement</span></span> | <span data-ttu-id="72867-118">Valor</span><span class="sxs-lookup"><span data-stu-id="72867-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72867-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72867-119">Minimum supported client</span></span><br/> | <span data-ttu-id="72867-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="72867-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="72867-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72867-121">Minimum supported server</span></span><br/> | <span data-ttu-id="72867-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72867-122">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="72867-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="72867-123">Namespace</span></span><br/>                | <span data-ttu-id="72867-124">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="72867-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="72867-125">MOF</span><span class="sxs-lookup"><span data-stu-id="72867-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72867-126"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72867-126"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="72867-127">DLL</span><span class="sxs-lookup"><span data-stu-id="72867-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72867-128"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72867-128"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72867-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="72867-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72867-130">**\_TSGetIcon Win32**</span><span class="sxs-lookup"><span data-stu-id="72867-130">**Win32\_TSGetIcon**</span></span>](win32-tsgeticon.md)
</dt> </dl>

 

 





