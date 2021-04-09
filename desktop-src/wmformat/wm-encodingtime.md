---
title: WM/Codificaçãotime
description: O atributo WM/Encodingtime contém um carimbo de data/hora da hora em que o conteúdo foi codificado.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Formato de mídia do WM/Encodingtime Windows
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006733"
---
# <a name="wmencodingtime"></a><span data-ttu-id="548a8-104">WM/Codificaçãotime</span><span class="sxs-lookup"><span data-stu-id="548a8-104">WM/EncodingTime</span></span>

<span data-ttu-id="548a8-105">O atributo **WM/encodingtime** contém um carimbo de data/hora da hora em que o conteúdo foi codificado.</span><span class="sxs-lookup"><span data-stu-id="548a8-105">The **WM/EncodingTime** attribute contains a time stamp of the time at which the content was encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="548a8-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="548a8-106">Global Constant</span></span>

<span data-ttu-id="548a8-107">g \_ wszWMEncodingTime</span><span class="sxs-lookup"><span data-stu-id="548a8-107">g\_wszWMEncodingTime</span></span>

## <a name="data-type"></a><span data-ttu-id="548a8-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="548a8-108">Data Type</span></span>

<span data-ttu-id="548a8-109">**FILETIME** (**WMT \_ tipo \_ QWORD**)</span><span class="sxs-lookup"><span data-stu-id="548a8-109">**FILETIME** (**WMT\_TYPE\_QWORD**)</span></span>

## <a name="remarks"></a><span data-ttu-id="548a8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="548a8-110">Remarks</span></span>

<span data-ttu-id="548a8-111">Esse atributo usa um valor FILETIME, que é um valor de 64 bits que representa o número de unidades de tempo de 100 nanossegundos decorridos desde 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="548a8-111">This attribute uses a FILETIME value, which is a 64-bit value representing the number of 100-nanosecond time units elapsed since January 1, 1601.</span></span> <span data-ttu-id="548a8-112">Para obter mais informações sobre o FILETIME, consulte a seção informações do sistema do Windows do SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="548a8-112">For more information about the FILETIME, see the Windows System Information section of the Platform SDK.</span></span>

<span data-ttu-id="548a8-113">Este não é um atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="548a8-113">This is not a coded attribute.</span></span> <span data-ttu-id="548a8-114">Você deve defini-lo manualmente se quiser incluí-lo em seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="548a8-114">You must set it manually if you want to include it in your files.</span></span>

## <a name="see-also"></a><span data-ttu-id="548a8-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="548a8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548a8-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="548a8-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




