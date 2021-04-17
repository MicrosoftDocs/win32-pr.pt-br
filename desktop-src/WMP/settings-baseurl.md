---
title: Settings. baseURL
description: A propriedade baseURL especifica ou recupera a URL base usada para a resolução de caminho relativa com comandos de script de URL inseridos em itens de mídia.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Settings. baseURL Windows Media Player
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748708"
---
# <a name="settingsbaseurl"></a><span data-ttu-id="511f7-104">Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="511f7-104">Settings.baseURL</span></span>

<span data-ttu-id="511f7-105">A propriedade **baseURL** especifica ou recupera a URL base usada para a resolução de caminho relativa com comandos de script de URL inseridos em itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="511f7-105">The **baseURL** property specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="511f7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="511f7-106">Syntax</span></span>

<span data-ttu-id="511f7-107">Player. Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="511f7-107">player.settings.baseURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="511f7-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="511f7-108">Possible Values</span></span>

<span data-ttu-id="511f7-109">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="511f7-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="511f7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="511f7-110">Remarks</span></span>

<span data-ttu-id="511f7-111">Essa propriedade especifica a URL HTTP base que é passada como o parâmetro de comando pelo evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="511f7-111">This property specifies the base HTTP URL that is passed as the command parameter by the **ScriptCommand** event.</span></span> <span data-ttu-id="511f7-112">A URL base é concatenada com a URL relativa da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="511f7-112">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="511f7-113">Uma barra (/) à direita é adicionada ao valor da propriedade **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="511f7-113">A trailing forward slash (/) is added to the value of the **baseURL** property.</span></span>
2.  <span data-ttu-id="511f7-114">Um período à esquerda, uma barra invertida ou uma barra (., \\ e/) são excluídos da URL relativa.</span><span class="sxs-lookup"><span data-stu-id="511f7-114">A leading period, backward slash, or forward slash (., \\, and /) are deleted from the relative URL.</span></span>
3.  <span data-ttu-id="511f7-115">A URL relativa é adicionada ao final da URL base.</span><span class="sxs-lookup"><span data-stu-id="511f7-115">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="511f7-116">Todas as barras na URL totalmente qualificada resultante são apontadas na mesma direção (convertida para barras para frente ou para trás) com base na direção do caractere de primeira barra encontrado na nova URL.</span><span class="sxs-lookup"><span data-stu-id="511f7-116">All slashes in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="511f7-117">**Observação**</span><span class="sxs-lookup"><span data-stu-id="511f7-117">**Note**</span></span>

<span data-ttu-id="511f7-118">O controle de jogador não dá suporte ao uso de dois pontos (..) na URL relativa para indicar o pai do local atual.</span><span class="sxs-lookup"><span data-stu-id="511f7-118">The player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

<span data-ttu-id="511f7-119">**Windows Media Player 10 Mobile**: essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="511f7-119">**Windows Media Player 10 Mobile**: This property is read-only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="511f7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="511f7-120">Requirements</span></span>



| <span data-ttu-id="511f7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="511f7-121">Requirement</span></span> | <span data-ttu-id="511f7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="511f7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="511f7-123">Versão</span><span class="sxs-lookup"><span data-stu-id="511f7-123">Version</span></span><br/> | <span data-ttu-id="511f7-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="511f7-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="511f7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="511f7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="511f7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="511f7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="511f7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="511f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511f7-128">**Evento Player. ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="511f7-128">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="511f7-129">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="511f7-129">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





