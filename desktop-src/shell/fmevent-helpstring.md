---
description: Enviado para um procedimento DLL de extensão do Gerenciador de arquivos quando o Gerenciador de arquivos quiser uma cadeia de caracteres de ajuda para um item de comando de menu ou barra de ferramentas
title: Mensagem de FMEVENT_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: 6fe187330e27f7e246c9bbd68005f68f346bbc90
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841277"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="045aa-103">Mensagem de FMEVENT de \_ ajuda</span><span class="sxs-lookup"><span data-stu-id="045aa-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="045aa-104">Enviado para um procedimento DLL de extensão do Gerenciador de arquivos quando o Gerenciador de arquivos quiser uma cadeia de caracteres de ajuda para um item de comando de menu ou barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="045aa-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="045aa-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="045aa-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="045aa-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="045aa-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="045aa-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="045aa-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="045aa-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="045aa-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="045aa-109">O endereço de uma estrutura de [**\_ HelpString do FMS**](fms-helpstring.md) que comunica dados de cadeia de caracteres de ajuda de item de comando.</span><span class="sxs-lookup"><span data-stu-id="045aa-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="045aa-110">A **estrutura \_ HelpString do FMS** identifica o item de comando para o qual uma cadeia de caracteres de ajuda é desejada, juntamente com um identificador para seu menu.</span><span class="sxs-lookup"><span data-stu-id="045aa-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="045aa-111">Em seguida, um aplicativo grava a cadeia de caracteres de ajuda apropriada para o membro **szHelp** da estrutura de **\_ HelpString do FMS** .</span><span class="sxs-lookup"><span data-stu-id="045aa-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="045aa-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="045aa-112">Return value</span></span>

<span data-ttu-id="045aa-113">Um procedimento de DLL de extensão deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="045aa-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="045aa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="045aa-114">Requirements</span></span>



| <span data-ttu-id="045aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="045aa-115">Requirement</span></span> | <span data-ttu-id="045aa-116">Valor</span><span class="sxs-lookup"><span data-stu-id="045aa-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="045aa-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="045aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="045aa-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="045aa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="045aa-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="045aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="045aa-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="045aa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="045aa-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="045aa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="045aa-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="045aa-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="045aa-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="045aa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="045aa-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="045aa-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="045aa-125">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="045aa-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




