---
title: WM/StreamTypeInfo
description: O atributo WM/StreamTypeInfo contém as informações de configuração para o fluxo especificado no arquivo ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Formato de mídia do Windows do WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364752"
---
# <a name="wmstreamtypeinfo"></a><span data-ttu-id="f8b09-104">WM/StreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="f8b09-104">WM/StreamTypeInfo</span></span>

<span data-ttu-id="f8b09-105">O atributo **WM/StreamTypeInfo** contém as informações de configuração para o fluxo especificado no arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="f8b09-105">The **WM/StreamTypeInfo** attribute contains the configuration information for the specified stream in the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f8b09-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="f8b09-106">Global Constant</span></span>

<span data-ttu-id="f8b09-107">g \_ wszWMStreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="f8b09-107">g\_wszWMStreamTypeInfo</span></span>

## <a name="data-type"></a><span data-ttu-id="f8b09-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f8b09-108">Data Type</span></span>

<span data-ttu-id="f8b09-109">[**WM \_ \_ \_ informações de tipo de fluxo**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT \_ tipo \_ Binary**)</span><span class="sxs-lookup"><span data-stu-id="f8b09-109">[**WM\_STREAM\_TYPE\_INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b09-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8b09-110">Remarks</span></span>

<span data-ttu-id="f8b09-111">Esse atributo se aplica a fluxos específicos.</span><span class="sxs-lookup"><span data-stu-id="f8b09-111">This attribute applies to specific streams.</span></span> <span data-ttu-id="f8b09-112">Você não pode recuperar este atributo para o fluxo 0.</span><span class="sxs-lookup"><span data-stu-id="f8b09-112">You cannot retrieve this attribute for stream 0.</span></span>

<span data-ttu-id="f8b09-113">Este atributo é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f8b09-113">This attribute is read-only.</span></span>

<span data-ttu-id="f8b09-114">O **WM/StreamTypeInfo** pode ser acessado pelo objeto editor de metadados.</span><span class="sxs-lookup"><span data-stu-id="f8b09-114">**WM/StreamTypeInfo** can be accessed by the metadata editor object.</span></span> <span data-ttu-id="f8b09-115">Essa é a única maneira de acessar as informações de configuração de fluxo sem abrir o arquivo com o objeto leitor (ou o objeto leitor síncrono).</span><span class="sxs-lookup"><span data-stu-id="f8b09-115">This is the only way to access stream configuration information without opening the file with the reader object (or the synchronous reader object).</span></span>

## <a name="see-also"></a><span data-ttu-id="f8b09-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8b09-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b09-117">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="f8b09-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




