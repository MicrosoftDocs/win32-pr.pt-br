---
description: o arquivo VBScript WiLstPrd.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. O script de exemplo se conecta a um objeto do instalador e enumera os produtos registrados e as informações do produto.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Listar produtos, propriedades, recursos e componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa090deef877757277b64cef02ecf42df61405fdc9238935bfffba756434f316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013144"
---
# <a name="list-products-properties-features-and-components"></a>Listar produtos, propriedades, recursos e componentes

o arquivo VBScript WiLstPrd.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). O script de exemplo se conecta a um objeto do [**instalador**](installer-object.md) e enumera os produtos registrados e as informações do produto.

Este exemplo demonstra o uso de:

-   [**Propriedade ProductInfo**](installer-productinfo.md)
-   [**Propriedade productstate (objeto do instalador)**](installer-productstate-property.md)
-   [**Propriedade Products**](installer-products.md)
-   [**Propriedade Features**](installer-features.md)
-   [**Propriedade FeatureParent**](installer-featureparent.md)
-   [**Propriedade featurestate**](installer-featurestate.md)
-   [**Propriedade Components**](installer-components.md)
-   [**Propriedade ComponentClients**](installer-componentclients.md)
-   [**Propriedade ComponentPath**](installer-componentpath.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md)
-   [**Método REGISTRYVALUE**](installer-registryvalue.md) do [ **objeto instalador**](installer-object.md)

você precisará da versão CScript.exe ou WScript.exe do Host de Script Windows para usar este exemplo. Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ caminho para o arquivo \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiLstPrd.vbs \[ Opções de nome do produto \] \[\]**

Especifique o nome do produto que não diferencia maiúsculas de minúsculas ou o GUID da ID do produto do produto instalado ou anunciado. Se nenhum produto ou opção for especificado, o instalador listará todos os produtos instalados ou anunciados no sistema.

Observe que essas opções não são opções, portanto, você não deve prefixar-as com uma barra (/) na linha de comando. As opções a seguir podem ser combinadas concatenando as letras. Por exemplo, "PC" para listar as propriedades dos produtos e os componentes instalados.



| Opção               | Descrição                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| nenhuma opção especificada | Listar as propriedades dos produtos.                                                                                                        |
| p                    | Listar as propriedades dos produtos.                                                                                                        |
| f                    | Listar os recursos dos produtos, os pais de recursos e os Estados de instalação                                                                 |
| c                    | Lista os componentes instalados dos produtos.                                                                                              |
| d                    | liste o valor em **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDlls** para os arquivos de chave do componente products. |



 

para obter mais informações, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md) para obter exemplos de script adicionais. para utilitários de exemplo que não exigem Windows Host de Script, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



