---
description: Depois de criar uma extensão de snap-in de anexo, você deve registrá-la para o MMC e os snap-ins de configuração de segurança para localizá-los e usá-los.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrando uma extensão de snap-in de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7af8b586f0071a5718b420612fd552d578bf30bb083cca45a43f38198e1aee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005014"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Registrando uma extensão de snap-in de anexo

Depois de criar uma extensão de snap-in de anexo, você deve registrá-la para o MMC e os snap-ins de configuração de segurança para localizá-los e usá-los.

Seu snap-in de anexo deve estender o namespace de snap-ins de configuração de segurança adicionando seu próprio nó, conforme descrito no procedimento a seguir.

**Para instalar e registrar a extensão de snap-in de anexo**

1.  Registre a extensão do snap-in na seguinte chave do registro. Não crie uma chave autônoma no snap-in; extensões de snap-ins de anexo só devem ser extensões.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  Registre a extensão de snap-in de anexo nas seguintes subchaves. Isso pode ser feito como parte das implementações de função **DllRegisterServer** e **DllUnregisterServer** .

    Namespace de [modelos de segurança](security-templates.md) :

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    [Configuração de segurança e namespace de análise](security-configuration-and-analysis.md) :

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



