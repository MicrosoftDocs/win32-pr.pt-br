---
title: Modificando atributos com ADSI
description: Para modificar valores de atributo, a ADSI fornece os métodos IADs. put e IADs. PutEx. Esses métodos modificam os dados no cache do lado do cliente. O método IADs. setinfo deve ser chamado para confirmar as alterações no diretório.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modificando atributos com ADSI
- Atributos ADSI, modificando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366710"
---
# <a name="modifying-attributes-with-adsi"></a><span data-ttu-id="7ffa6-107">Modificando atributos com ADSI</span><span class="sxs-lookup"><span data-stu-id="7ffa6-107">Modifying Attributes with ADSI</span></span>

<span data-ttu-id="7ffa6-108">Para modificar valores de atributo, a ADSI fornece os métodos [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="7ffa6-108">To modify attribute values, ADSI provides the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) methods.</span></span> <span data-ttu-id="7ffa6-109">Esses métodos modificam os dados no cache do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-109">These methods modify the data on the client-side cache.</span></span> <span data-ttu-id="7ffa6-110">O método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) deve ser chamado para confirmar as alterações no diretório.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-110">The [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method must be called to commit the changes to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="7ffa6-111">Quando várias alterações de atributo são confirmadas em uma única chamada para [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), se qualquer atributo único não puder ser modificado, nenhum dos atributos será modificado.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-111">When multiple attribute changes are committed in a single call to [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), if any single attribute cannot be modified, none of the attributes will be modified.</span></span> <span data-ttu-id="7ffa6-112">Por exemplo, se você modificar os atributos [**SN**](/windows/desktop/ADSchema/a-sn) e [**excertoname**](/windows/desktop/ADSchema/a-givenname) e limpar o atributo [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) de um objeto de usuário sem nenhuma chamada subsequente para o método **setinfo** , as alterações serão inseridas quando você chamar **setinfo**.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-112">For example, if you modify the [**sn**](/windows/desktop/ADSchema/a-sn) and [**givenName**](/windows/desktop/ADSchema/a-givenname) attributes and clear the [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) attribute of a user object without any subsequent calls to the **SetInfo** method, the changes are entered when you call **SetInfo**.</span></span> <span data-ttu-id="7ffa6-113">Se uma ou mais das modificações não forem permitidas e, portanto, não puderem ser executadas, nenhuma das modificações coletiva feitas nos atributos será inserida durante a chamada para **setinfo**.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-113">If one or more of the modifications are not allowed and therefore cannot be performed, then none of the collective modifications made to the attributes are entered during the call to **SetInfo**.</span></span>

 

<span data-ttu-id="7ffa6-114">O método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) usa um nome de atributo e um parâmetro VARIANT.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-114">The [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method takes an attribute name and a variant parameter.</span></span> <span data-ttu-id="7ffa6-115">Use este método para definir atributos que contêm valores únicos e múltiplos.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-115">Use this method to set attributes that contain both single and multiple values.</span></span>

<span data-ttu-id="7ffa6-116">O método [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) fornece controle sobre as operações em atributos com valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-116">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method provides control over operations on multi-valued attributes.</span></span> <span data-ttu-id="7ffa6-117">Você pode acrescentar, excluir, atualizar e limpar os valores existentes.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-117">You can append, delete, update, and clear existing values.</span></span> <span data-ttu-id="7ffa6-118">O método **IADs. PutEx** sempre espera uma matriz variante de valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-118">The **IADs.PutEx** method always expects a variant array of attribute values.</span></span> <span data-ttu-id="7ffa6-119">No entanto, você pode usar esse método para definir um atributo com um único valor também.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-119">However, you can use this method to set an attribute with a single value as well.</span></span>

<span data-ttu-id="7ffa6-120">O método [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa as operações especificadas pela enumeração [**\_ enum da \_ operação \_ de propriedade ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="7ffa6-120">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the operations specified by the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

 

 