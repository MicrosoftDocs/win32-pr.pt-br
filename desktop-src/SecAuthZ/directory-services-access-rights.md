---
description: Cada objeto de Active Directory tem um descritor de segurança atribuído a ele.
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: Direitos de acesso aos serviços de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901c8eba5736750e0c91eb713993876c47858407110ca3c8ebc6ed8122e1b8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913759"
---
# <a name="directory-services-access-rights"></a>Direitos de acesso aos serviços de diretório

Cada objeto de Active Directory tem um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) atribuído a ele. Um conjunto de direitos de confiança específico para objetos de serviço de diretório pode ser definido dentro desses descritores de segurança. Esses direitos são listados na tabela a seguir. Para obter mais informações, consulte [controlar direitos de acesso](/windows/desktop/AD/control-access-rights).



| Direitos                                | Significado                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTRL \_ DS \_ aberto<br/>            | Abra um objeto DS.<br/>                                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ Create \_ filho<br/>   | Crie um objeto DS filho.<br/>                                                                                                                                                                                                                                                    |
| filho de exclusão do ACTRL \_ DS \_ \_<br/>   | Excluir um objeto DS filho.<br/>                                                                                                                                                                                                                                                    |
| \_lista de DS do ACTRL \_<br/>            | Enumere um objeto DS.<br/>                                                                                                                                                                                                                                                       |
| PROP ACTRL de \_ leitura do DS \_ \_<br/>      | Ler as propriedades de um objeto DS.<br/>                                                                                                                                                                                                                                          |
| PROP ACTRL de \_ \_ gravação DS \_<br/>     | Gravar propriedades para um objeto DS.<br/>                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ próprio<br/>            | Acesso permitido somente depois que as verificações de direitos validadas com suporte pelo objeto forem executadas. Esse sinalizador pode ser usado sozinho para executar todas as verificações de direitos validadas do objeto ou pode ser combinado com um identificador de um direito validado específico para executar apenas essa verificação.<br/> |
| árvore de exclusão do ACTRL \_ DS \_ \_<br/>    | Exclua uma árvore de objetos DS.<br/>                                                                                                                                                                                                                                                 |
| \_objeto de \_ lista \_ DS do ACTRL<br/>    | Liste uma árvore de objetos DS.<br/>                                                                                                                                                                                                                                                   |
| \_acesso de \_ controle \_ DS ACTRL<br/> | Acesso permitido somente depois que as verificações de direitos estendidas com suporte pelo objeto são executadas. Esse sinalizador pode ser usado sozinho para executar todas as verificações de direitos estendidas no objeto ou pode ser combinado com um identificador de um direito estendido específico para executar apenas essa verificação.<br/>    |



 

 

