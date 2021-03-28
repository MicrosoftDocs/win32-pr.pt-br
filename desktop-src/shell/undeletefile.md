---
description: Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos quando o usuário escolhe o comando restaurar no menu arquivo.
title: Ponteiro de função FM_UNDELETE_PROC (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171545"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="5e715-103">\_ \_ Ponteiro da função proc de exclusão de FM</span><span class="sxs-lookup"><span data-stu-id="5e715-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="5e715-104">Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos quando o usuário escolhe o comando **restaurar** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="5e715-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e715-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e715-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="5e715-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e715-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="5e715-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="5e715-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="5e715-108">Type: **HWND**</span></span>

<span data-ttu-id="5e715-109">O identificador de janela para o Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5e715-109">The window handle to File Manager.</span></span> <span data-ttu-id="5e715-110">Uma DLL de exclusão deve usar esse identificador para especificar a janela do proprietário de qualquer caixa de diálogo ou caixa de mensagem que a DLL possa exibir.</span><span class="sxs-lookup"><span data-stu-id="5e715-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="5e715-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="5e715-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="5e715-112">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="5e715-112">Type: **LPSTR**</span></span>

<span data-ttu-id="5e715-113">O endereço de uma cadeia de caracteres terminada em nulo que contém o nome do diretório inicial.</span><span class="sxs-lookup"><span data-stu-id="5e715-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e715-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e715-114">Return value</span></span>

<span data-ttu-id="5e715-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5e715-115">Type: **DWORD**</span></span>

<span data-ttu-id="5e715-116">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e715-116">Returns one of the following values.</span></span>



| <span data-ttu-id="5e715-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5e715-117">Return code</span></span>                                                                             | <span data-ttu-id="5e715-118">Description</span><span class="sxs-lookup"><span data-stu-id="5e715-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e715-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="5e715-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="5e715-120">Ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="5e715-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="5e715-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e715-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="5e715-122">Um arquivo não foi excluído.</span><span class="sxs-lookup"><span data-stu-id="5e715-122">A file was undeleted.</span></span> <span data-ttu-id="5e715-123">O Gerenciador de arquivos redesenha sua janela.</span><span class="sxs-lookup"><span data-stu-id="5e715-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="5e715-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="5e715-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="5e715-125">Nenhum arquivo foi reexcluído.</span><span class="sxs-lookup"><span data-stu-id="5e715-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="5e715-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e715-126">Requirements</span></span>



| <span data-ttu-id="5e715-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e715-127">Requirement</span></span> | <span data-ttu-id="5e715-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5e715-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e715-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e715-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5e715-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5e715-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e715-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e715-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5e715-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e715-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e715-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5e715-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e715-134"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e715-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




