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
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842417"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="d44cb-103">\_ \_ Ponteiro da função proc de exclusão de FM</span><span class="sxs-lookup"><span data-stu-id="d44cb-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="d44cb-104">Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos quando o usuário escolhe o comando **restaurar** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="d44cb-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="d44cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d44cb-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="d44cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d44cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d44cb-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="d44cb-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="d44cb-108">Digite: **HWND**</span><span class="sxs-lookup"><span data-stu-id="d44cb-108">Type: **HWND**</span></span>

<span data-ttu-id="d44cb-109">O identificador de janela para o Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d44cb-109">The window handle to File Manager.</span></span> <span data-ttu-id="d44cb-110">Uma DLL de exclusão deve usar esse identificador para especificar a janela do proprietário de qualquer caixa de diálogo ou caixa de mensagem que a DLL possa exibir.</span><span class="sxs-lookup"><span data-stu-id="d44cb-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="d44cb-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="d44cb-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="d44cb-112">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="d44cb-112">Type: **LPSTR**</span></span>

<span data-ttu-id="d44cb-113">O endereço de uma cadeia de caracteres terminada em nulo que contém o nome do diretório inicial.</span><span class="sxs-lookup"><span data-stu-id="d44cb-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d44cb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d44cb-114">Return value</span></span>

<span data-ttu-id="d44cb-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d44cb-115">Type: **DWORD**</span></span>

<span data-ttu-id="d44cb-116">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d44cb-116">Returns one of the following values.</span></span>



| <span data-ttu-id="d44cb-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d44cb-117">Return code</span></span>                                                                             | <span data-ttu-id="d44cb-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d44cb-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d44cb-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="d44cb-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="d44cb-120">Ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="d44cb-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d44cb-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="d44cb-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="d44cb-122">Um arquivo não foi excluído.</span><span class="sxs-lookup"><span data-stu-id="d44cb-122">A file was undeleted.</span></span> <span data-ttu-id="d44cb-123">O Gerenciador de arquivos redesenha sua janela.</span><span class="sxs-lookup"><span data-stu-id="d44cb-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="d44cb-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="d44cb-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="d44cb-125">Nenhum arquivo foi reexcluído.</span><span class="sxs-lookup"><span data-stu-id="d44cb-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="d44cb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d44cb-126">Requirements</span></span>



| <span data-ttu-id="d44cb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d44cb-127">Requirement</span></span> | <span data-ttu-id="d44cb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d44cb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d44cb-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d44cb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d44cb-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d44cb-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d44cb-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d44cb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d44cb-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d44cb-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d44cb-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d44cb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d44cb-134"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="d44cb-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




