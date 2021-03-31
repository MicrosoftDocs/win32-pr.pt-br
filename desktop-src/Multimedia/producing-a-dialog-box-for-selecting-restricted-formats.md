---
title: Produzindo uma caixa de diálogo para selecionar formatos restritos
description: Produzindo uma caixa de diálogo para selecionar formatos restritos
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Gerenciador de compactação de áudio (ACM), produzindo caixas de diálogo
- ACM (Gerenciador de compactação de áudio), caixas de diálogo em produção
- Exemplos do ACM, caixas de diálogo de produção
- produzindo caixas de diálogo
- função acmFormatChoose
- Gerenciador de compactação de áudio (ACM), selecionando formatos restritos
- ACM (Gerenciador de compactação de áudio), selecionando formatos restritos
- Exemplos do ACM, seleção de formatos restritos
- selecionando formatos restritos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005651"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a><span data-ttu-id="ddbf2-112">Produzindo uma caixa de diálogo para selecionar formatos restritos</span><span class="sxs-lookup"><span data-stu-id="ddbf2-112">Producing a Dialog Box for Selecting Restricted Formats</span></span>

<span data-ttu-id="ddbf2-113">Talvez você queira usar a caixa de diálogo criada pela função [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , mas limitar ou controlar os formatos na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-113">You might want to use the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, but limit or control the formats in the dialog box.</span></span> <span data-ttu-id="ddbf2-114">Você pode fazer isso usando o sinalizador ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK para conectar o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-114">You can do this by using the ACMFORMATCHOOSE\_STYLEF\_ENABLEHOOK flag to hook the dialog procedure.</span></span> <span data-ttu-id="ddbf2-115">O aplicativo pode, então, filtrar os formatos respondendo à mensagem [**mm \_ ACM \_ FORMATCHOOSE**](mm-acm-formatchoose.md) no procedimento de mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ddbf2-115">The application can then filter the formats by responding to the [**MM\_ACM\_FORMATCHOOSE**](mm-acm-formatchoose.md) message in the message procedure for the dialog box.</span></span>

 

 




