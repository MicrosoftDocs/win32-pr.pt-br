---
title: Insertável (chave CLSID)
description: Indica que os objetos dessa classe devem aparecer na caixa de listagem da caixa de diálogo Inserir objeto quando usados por aplicativos de contêiner COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- COM chave de registro insertável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008754"
---
# <a name="insertable-clsid-key"></a><span data-ttu-id="f3ea0-104">Insertável (chave CLSID)</span><span class="sxs-lookup"><span data-stu-id="f3ea0-104">Insertable (CLSID Key)</span></span>

<span data-ttu-id="f3ea0-105">Indica que os objetos dessa classe devem aparecer na caixa de listagem da caixa de diálogo **Inserir objeto** quando usados por aplicativos de contêiner com.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-105">Indicates that objects of this class should appear in the **Insert Object** dialog box list box when used by COM container applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f3ea0-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="f3ea0-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a><span data-ttu-id="f3ea0-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3ea0-107">Remarks</span></span>

<span data-ttu-id="f3ea0-108">Essa chave é uma entrada necessária para aplicativos COM de 32 bits cujos objetos podem ser inseridos em aplicativos de 16 bits existentes.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-108">This key is a required entry for 32-bit COM applications whose objects can be inserted into existing 16-bit applications.</span></span> <span data-ttu-id="f3ea0-109">Os aplicativos de 16 bits existentes examinam o registro para essa chave, que informa ao aplicativo que o servidor oferece suporte a incorporações.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-109">Existing 16-bit applications look in the registry for this key, which informs the application that the server supports embeddings.</span></span> <span data-ttu-id="f3ea0-110">Se a chave que pode ser **inserida** existir, os aplicativos de 16 bits também poderão tentar verificar se o servidor existe no computador.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-110">If the **Insertable** key exists, 16-bit applications may also attempt to verify that the server exists on the machine.</span></span> <span data-ttu-id="f3ea0-111">Normalmente, os aplicativos de 16 bits recuperam o valor da chave [**LocalServer**](localserver.md) da classe e verificam se ele é um arquivo válido no sistema.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-111">16-bit applications typically retrieve the value of the [**LocalServer**](localserver.md) key from the class and check to see whether it is a valid file on the system.</span></span> <span data-ttu-id="f3ea0-112">Portanto, para que um aplicativo de 32 bits seja inserido por um aplicativo de 16 bits, o aplicativo de 32 bits deve registrar a subchave **LocalServer** , além de registrar [**LocalServer32**](localserver32.md).</span><span class="sxs-lookup"><span data-stu-id="f3ea0-112">Therefore, for a 32-bit application to be insertable by a 16-bit application, the 32-bit application should register the **LocalServer** subkey in addition to registering [**LocalServer32**](localserver32.md).</span></span>

<span data-ttu-id="f3ea0-113">Usado com controles, essa entrada indica que um objeto pode agir somente como um objeto inserido in-loco sem recursos de controle especiais.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-113">Used with controls, this entry indicates that an object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="f3ea0-114">Os objetos que têm essa chave aparecem na caixa de diálogo **Inserir objeto** para seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-114">Objects that have this key appear in the **Insert Object** dialog box for their container.</span></span> <span data-ttu-id="f3ea0-115">Quando usado com controles, essa entrada também indica que o controle foi testado com contêineres que não são de controle.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-115">When used with controls, this entry also indicates the control has been tested with non-control containers.</span></span> <span data-ttu-id="f3ea0-116">Essa entrada também é opcional e pode ser omitida quando um controle não é projetado para funcionar com contêineres mais antigos que não entendem controles.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-116">This entry is also optional and can be omitted when a control is not designed to work with older containers that do not understand controls.</span></span>

> [!Note]  
> <span data-ttu-id="f3ea0-117">Essa chave não está presente para classes internas como as classes moniker.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-117">This key is not present for internal classes like the moniker classes.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3ea0-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3ea0-118">Related topics</span></span>

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




