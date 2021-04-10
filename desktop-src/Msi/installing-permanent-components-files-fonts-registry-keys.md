---
description: Para instalar um arquivo, uma fonte ou uma chave do registro para que ele não seja removido quando o produto for desinstalado, todo o componente que contém o arquivo, a fonte ou a chave do registro deverá se tornar permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Instalando componentes, arquivos, fontes e chaves do registro permanentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011814"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a><span data-ttu-id="0fcfa-103">Instalando componentes, arquivos, fontes e chaves do registro permanentes</span><span class="sxs-lookup"><span data-stu-id="0fcfa-103">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>

<span data-ttu-id="0fcfa-104">Para instalar um arquivo, uma fonte ou uma chave do registro para que ele não seja removido quando o produto for desinstalado, todo o componente que contém o arquivo, a fonte ou a chave do registro deverá se tornar permanente.</span><span class="sxs-lookup"><span data-stu-id="0fcfa-104">To install a file, font, or registry key so that it is not removed when the product is uninstalled, the entire component containing the file, font, or registry key must be made permanent.</span></span> <span data-ttu-id="0fcfa-105">Para tornar um componente permanente, defina **msidbComponentAttributesPermanent** na coluna atributos da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0fcfa-105">To make a component permanent, set **msidbComponentAttributesPermanent** in the Attributes column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="0fcfa-106">Observe que o instalador remove uma chave do registro depois de remover o último valor ou subchave sob a chave.</span><span class="sxs-lookup"><span data-stu-id="0fcfa-106">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="0fcfa-107">Para impedir que uma chave do registro vazia seja removida na desinstalação, grave um valor fictício sob a chave que você precisa manter e digite + na coluna nome da [tabela do registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="0fcfa-107">To prevent an empty registry key from being removed on uninstall, write a dummy value under the key you need keep, and enter + in the Name column of the [Registry table](registry-table.md).</span></span>

 

 



