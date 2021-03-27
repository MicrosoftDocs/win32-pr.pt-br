---
description: 'Permite que o objeto de retorno de chamada especifique um arquivo de ajuda HTML e um tópico dentro dele. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_GETHELPTOPIC (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829219"
---
# <a name="sfvm_gethelptopic-message"></a><span data-ttu-id="b970b-104">\_Mensagem SFVM GETHELPTOPIC</span><span class="sxs-lookup"><span data-stu-id="b970b-104">SFVM\_GETHELPTOPIC message</span></span>

<span data-ttu-id="b970b-105">Permite que o objeto de retorno de chamada especifique um arquivo de ajuda HTML e um tópico dentro dele.</span><span class="sxs-lookup"><span data-stu-id="b970b-105">Allows the callback object to specify an HTML Help file and a topic within it.</span></span> <span data-ttu-id="b970b-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="b970b-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a><span data-ttu-id="b970b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b970b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b970b-108">*PHTD* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b970b-108">*phtd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b970b-109">O endereço de uma estrutura de [**\_ \_ dados SFVM HELPTOPIC**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) que especifica o tópico e o arquivo de ajuda HTML.</span><span class="sxs-lookup"><span data-stu-id="b970b-109">The address of a [**SFVM\_HELPTOPIC\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) structure that specifies the HTML Help file and topic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b970b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b970b-110">Requirements</span></span>



| <span data-ttu-id="b970b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b970b-111">Requirement</span></span> | <span data-ttu-id="b970b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b970b-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b970b-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b970b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b970b-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b970b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b970b-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b970b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b970b-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b970b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b970b-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b970b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b970b-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b970b-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
