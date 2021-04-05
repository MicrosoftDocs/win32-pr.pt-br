---
description: Inserção de quadro-chave forçada
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserção de quadro-chave forçada (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457213"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a><span data-ttu-id="02d74-103">Inserção de quadro-chave forçada (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="02d74-103">Forced Key Frame Insertion (Microsoft Media Foundation)</span></span>

<span data-ttu-id="02d74-104">Ao configurar um objeto de codificador de vídeo, você pode definir um intervalo máximo para quadros-chave no conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="02d74-104">When you configure a video encoder object, you can set a maximum interval for key frames in the encoded content.</span></span> <span data-ttu-id="02d74-105">No entanto, o codec irá posicionar os quadros-chave dentro desse intervalo, conforme determinado pelo conteúdo; o intervalo de quadros chave não é constante.</span><span class="sxs-lookup"><span data-stu-id="02d74-105">However, the codec will place key frames within that interval as dictated by the content; the key frame interval is not constant.</span></span> <span data-ttu-id="02d74-106">Para alguns aplicativos, a distância do quadro chave é muito importante.</span><span class="sxs-lookup"><span data-stu-id="02d74-106">For some applications, the key frame distance is very important.</span></span> <span data-ttu-id="02d74-107">Por exemplo, um aplicativo de edição de vídeo precisa de quadros-chave em locais que são lógicos a um editor, como em quebras de cena e transições de captura.</span><span class="sxs-lookup"><span data-stu-id="02d74-107">For example, a video editing application needs key frames at locations that are logical to an editor, like at scene breaks and shot transitions.</span></span>

<span data-ttu-id="02d74-108">A inserção de quadro-chave forçada é um recurso que permite solicitar que um quadro de entrada seja codificado como um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="02d74-108">Forced key frame insertion is a feature that enables you to request that an input frame be encoded as a key frame.</span></span> <span data-ttu-id="02d74-109">O codificador tentará respeitar essas solicitações, mas as configurações de buffer (taxa de bits e janela de buffer) configuradas para a sessão de codificação sempre terão precedência.</span><span class="sxs-lookup"><span data-stu-id="02d74-109">The encoder will try to honor these requests, but the buffer settings (bit rate and buffer window) configured for the encoding session always take precedence.</span></span>

<span data-ttu-id="02d74-110">Os objetos do codificador de vídeo implementam a inserção de quadro chave forçado como uma resposta a uma extensão de unidade de dados anexada ao exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="02d74-110">The video encoder objects implement forced key frame insertion as a response to a data unit extension attached to the input sample.</span></span> <span data-ttu-id="02d74-111">Para obter mais informações sobre extensões de unidade de dados, consulte [usando extensões de unidade de dados](usingdataunitextensions.md).</span><span class="sxs-lookup"><span data-stu-id="02d74-111">For more information about data unit extensions, see [Using Data Unit Extensions](usingdataunitextensions.md).</span></span>

<span data-ttu-id="02d74-112">Os dados de extensão para a inserção de quadro de chave forçada são identificados pelo seguinte valor de GUID: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span><span class="sxs-lookup"><span data-stu-id="02d74-112">The extension data for forced key frame insertion is identified by the following GUID value: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span></span> <span data-ttu-id="02d74-113">As extensões individuais são valores **bool** .</span><span class="sxs-lookup"><span data-stu-id="02d74-113">The individual extensions are **BOOL** values.</span></span> <span data-ttu-id="02d74-114">Defina o valor como **true** para indicar uma solicitação de quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="02d74-114">Set the value to **TRUE** to indicate a key frame request.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02d74-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02d74-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02d74-116">Usando extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="02d74-116">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
</dt> <dt>

[<span data-ttu-id="02d74-117">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="02d74-117">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



