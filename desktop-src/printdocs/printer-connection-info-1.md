---
description: Representa informações sobre uma conexão a uma impressora.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Estrutura de PRINTER_CONNECTION_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662449"
---
# <a name="printer_connection_info_1-structure"></a><span data-ttu-id="47cc0-103">Estrutura de informações de conexão da impressora \_ \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="47cc0-103">PRINTER\_CONNECTION\_INFO\_1 structure</span></span>

<span data-ttu-id="47cc0-104">Representa informações sobre uma conexão a uma impressora.</span><span class="sxs-lookup"><span data-stu-id="47cc0-104">Represents information about a connection to a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="47cc0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47cc0-105">Syntax</span></span>


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a><span data-ttu-id="47cc0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="47cc0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="47cc0-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="47cc0-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="47cc0-108">Os seguintes valores são definidos:</span><span class="sxs-lookup"><span data-stu-id="47cc0-108">The following values are defined:</span></span>



| <span data-ttu-id="47cc0-109">Valor</span><span class="sxs-lookup"><span data-stu-id="47cc0-109">Value</span></span>                                      | <span data-ttu-id="47cc0-110">Significado</span><span class="sxs-lookup"><span data-stu-id="47cc0-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47cc0-111">\_Incompatibilidade \_ de conexão de impressora (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="47cc0-111">PRINTER\_CONNECTION\_MISMATCH (0x00000020)</span></span> | <span data-ttu-id="47cc0-112">Se esse sinalizador de bit estiver definido, a conexão de impressora não corresponde.</span><span class="sxs-lookup"><span data-stu-id="47cc0-112">If this bit-flag is set, the printer connection is mismatched.</span></span> <span data-ttu-id="47cc0-113">O usuário pode fornecer um driver de impressão local como *pszDriverName* e usá-lo para fazer a renderização em vez de usar o driver instalado na impressora do servidor à qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="47cc0-113">The user can supply a local print driver as *pszDriverName* and use it to do the rendering instead of using the driver installed on the server printer to which the user is connected.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="47cc0-114">\_Conexão \_ de impressora sem \_ interface do usuário (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="47cc0-114">PRINTER\_CONNECTION\_NO\_UI (0x00000040)</span></span>   | <span data-ttu-id="47cc0-115">Se esse sinalizador de bit estiver definido, essa chamada não poderá exibir uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="47cc0-115">If this bit-flag is set then this call cannot display a dialog box.</span></span> <span data-ttu-id="47cc0-116">Se for necessário exibir uma caixa de diálogo para instalar um driver de impressora a partir do servidor e esse sinalizador de bits estiver definido, o driver de impressora não será adicionado e a chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="47cc0-116">If a dialog box must be displayed to install a printer driver from the server and this bit-flag is set, the printer driver will not be installed, the printer connection will not be added, and the call will fail.</span></span><br/> <span data-ttu-id="47cc0-117">**Windows 7:** No Windows 7 e versões posteriores do Windows, se esse sinalizador estiver definido e o usuário estiver sendo executado no modo elevado, a caixa de diálogo **você confia nesta impressora?** não será exibida.</span><span class="sxs-lookup"><span data-stu-id="47cc0-117">**Windows 7:** In Windows 7 and later versions of Windows, if this flag is set and the user is running in elevated mode, the **Do you trust this printer?** dialog will not be shown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="47cc0-118">**pszDriverName**</span><span class="sxs-lookup"><span data-stu-id="47cc0-118">**pszDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="47cc0-119">Um ponteiro para o nome do driver.</span><span class="sxs-lookup"><span data-stu-id="47cc0-119">A pointer to the name of the driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47cc0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47cc0-120">Requirements</span></span>



| <span data-ttu-id="47cc0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="47cc0-121">Requirement</span></span> | <span data-ttu-id="47cc0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="47cc0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47cc0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47cc0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="47cc0-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47cc0-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="47cc0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47cc0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="47cc0-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47cc0-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="47cc0-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47cc0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="47cc0-128"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47cc0-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47cc0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="47cc0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47cc0-130">Impressão</span><span class="sxs-lookup"><span data-stu-id="47cc0-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="47cc0-131">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="47cc0-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




