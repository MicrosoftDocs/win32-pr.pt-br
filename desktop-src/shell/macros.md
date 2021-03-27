---
description: Esta seção descreve as macros do utilitário de shell do Windows.
title: Macros do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 085bca918cfa6ca1441272c3c9181226ef603ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921983"
---
# <a name="shell-macros"></a><span data-ttu-id="804d8-103">Macros do Shell</span><span class="sxs-lookup"><span data-stu-id="804d8-103">Shell Macros</span></span>

<span data-ttu-id="804d8-104">Esta seção descreve as macros do utilitário de shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="804d8-104">This section describes the Windows Shell utility macros.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="804d8-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="804d8-105">In this section</span></span>



| <span data-ttu-id="804d8-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="804d8-106">Topic</span></span>                                                                  | <span data-ttu-id="804d8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="804d8-107">Description</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="804d8-108">**DEFINIR \_ PROPERTYKEY**</span><span class="sxs-lookup"><span data-stu-id="804d8-108">**DEFINE\_PROPERTYKEY**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | <span data-ttu-id="804d8-109">Usado para empacotar um identificador de formato (FMTID) e um identificador de propriedade (PID) em uma estrutura [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) que representa uma chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="804d8-109">Used to pack a format identifier (FMTID) and property identifier (PID) into a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure that represents a property key.</span></span><br/>                                                                                    |
| [<span data-ttu-id="804d8-110">**\_argumentos de PPV de IID \_**</span><span class="sxs-lookup"><span data-stu-id="804d8-110">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | <span data-ttu-id="804d8-111">Usado para recuperar um ponteiro de interface, fornecendo o valor de IID da interface solicitada automaticamente com base no tipo de ponteiro de interface usado.</span><span class="sxs-lookup"><span data-stu-id="804d8-111">Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used.</span></span> <span data-ttu-id="804d8-112">Isso evita um erro de codificação comum, verificando o tipo do valor passado no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="804d8-112">This avoids a common coding error by checking the type of the value passed at compile time.</span></span><br/> |
| [<span data-ttu-id="804d8-113">**IsEqualPropertyKey**</span><span class="sxs-lookup"><span data-stu-id="804d8-113">**IsEqualPropertyKey**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | <span data-ttu-id="804d8-114">Compara os membros de duas estruturas [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) e retorna se são iguais.</span><span class="sxs-lookup"><span data-stu-id="804d8-114">Compares the members of two [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structures and returns whether they are equal.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="804d8-115">**MAKEDLLVERULL**</span><span class="sxs-lookup"><span data-stu-id="804d8-115">**MAKEDLLVERULL**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | <span data-ttu-id="804d8-116">Usado para empacotar informações de versão de DLL em um valor ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="804d8-116">Used to pack DLL version information into a ULONGLONG value.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="804d8-117">**DisplayErrorTip de NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="804d8-117">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | <span data-ttu-id="804d8-118">Exibe uma mensagem de erro na dica de balão associada ao controle de endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="804d8-118">Displays an error message in the balloon tip associated with the network address control.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="804d8-119">**Getendereço GetAddr \_**</span><span class="sxs-lookup"><span data-stu-id="804d8-119">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | <span data-ttu-id="804d8-120">Indica se um endereço de rede está de acordo com um tipo e formato especificados.</span><span class="sxs-lookup"><span data-stu-id="804d8-120">Indicates whether a network address conforms to a specified type and format.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="804d8-121">**Getallowtype de NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="804d8-121">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | <span data-ttu-id="804d8-122">Recupera os tipos de endereço de rede que um controle de endereço de rede especificado aceita.</span><span class="sxs-lookup"><span data-stu-id="804d8-122">Retrieves the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="804d8-123">**SetAllowType de NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="804d8-123">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | <span data-ttu-id="804d8-124">Define os tipos de endereço de rede que um controle de endereço de rede especificado aceita.</span><span class="sxs-lookup"><span data-stu-id="804d8-124">Sets the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                     |



 

 

 
