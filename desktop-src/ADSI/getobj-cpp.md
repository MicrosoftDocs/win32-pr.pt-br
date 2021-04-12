---
title: GETOBJ. CPP
description: No componente do provedor de exemplo, aparece um exemplo de código usado para localizar e associar objetos em Getobj. cpp. As rotinas com suporte são listadas na tabela a seguir.
ms.assetid: d202e5ec-27b5-4809-a7fa-4a2e39c65295
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d58647208c68437c068d58cd9908bc08989141
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294502"
---
# <a name="getobjcpp"></a>GETOBJ. CPP

No componente do provedor de exemplo, aparece um exemplo de código usado para localizar e associar objetos em Getobj. cpp. As rotinas com suporte são listadas na tabela a seguir.



| Item                                | Descrição                                                                                                                                                                                                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RelativeGetObject**               | Obtém um objeto relativo a um determinado ADsPath.                                                                                                                                                                                                                                                       |
| **GetObject**                       | Chama **ADsObject** (Parse. cpp) para verificar a sintaxe do caminho, valida se o caminho tem o token do provedor correto e valida o tipo de objeto. Se não houver nenhum erro, crie uma instância do tipo correto de objeto e recupere um ponteiro para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do objeto. |
| **BuildADsPathFromDSPath**          | Criou uma cadeia de caracteres ADsPath a partir do caminho do diretório nativo.                                                                                                                                                                                                                                           |
| **BuildDSTreeNameFromADsPath**      | Use o ADsPath para criar um caminho de diretório de árvore possível para o caminho do diretório nativo.                                                                                                                                                                                                           |
| **BuildDSPathFromADsPath**          | Usa ADsPath e DSPathName.                                                                                                                                                                                                                                                                      |
| **BuildADsParentPath**              | Crie o ADsPath para o pai deste objeto.                                                                                                                                                                                                                                                  |
| **Getnamespaceobject**              | Valide e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em um exemplo de objeto de namespace.                                                                                                                                                                                                           |
| **ValidateNamespaceObject**         | Verifique se o objeto namespace corresponde ao nome do provedor atual.                                                                                                                                                                                                                               |
| **Validarprovider**                | Validar o nome do provedor (diferencia maiúsculas de minúsculas).                                                                                                                                                                                                                                                          |
| **GetSchemaObject**                 | Valide e abra o tipo de objeto de esquema apropriado. Em seguida, crie a correta e recupere o ponteiro da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) nela.                                                                                                                                        |
| **ValidateSchemaObject**            | Verifique se é um tipo de objeto de esquema válido.                                                                                                                                                                                                                                                     |
| **ValidateObjectType**              | Verifique se o tipo de objeto existe no esquema.                                                                                                                                                                                                                                                 |
| **BuildSampleDSRootRDNFromADsPath** | Crie o ADsPath para o nó raiz do componente de provedor de exemplo.                                                                                                                                                                                                                            |
| **BuildDSPathFromADsPath**          | Usa ADsPath, DSRootRDN e DSPathName.                                                                                                                                                                                                                                                          |



 

 

 