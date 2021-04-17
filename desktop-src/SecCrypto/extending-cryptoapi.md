---
description: O CryptoAPI foi projetado para ser facilmente extensível. Novos tipos e parâmetros podem ser definidos por qualquer autor do CSP (provedor de serviços de criptografia) para fazer com que o CryptoAPI Curve os requisitos de uma ampla variedade de situações.
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: Estendendo o CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62417f66b8a8bb2d06d145543f944f91868d366d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757072"
---
# <a name="extending-cryptoapi"></a>Estendendo o CryptoAPI

O [*CryptoAPI*](../secgloss/c-gly.md) foi projetado para ser facilmente extensível. Novos tipos e parâmetros podem ser definidos por qualquer autor do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para fazer com que o CryptoAPI Curve os requisitos de uma ampla variedade de situações.



| Itens extensíveis                                                                                                 | Comentário                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipos de provedor<br/>                                                                                        | Um tipo de provedor representa uma família específica ou tipo de serviços de criptografia. Novos tipos de provedor podem ser definidos, cada um atendendo a um nicho específico.<br/>                                                                                                                                                                                                                                                                                          |
| Parâmetros do provedor<br/>                                                                                   | Os parâmetros do provedor são enviados e recebidos usando [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) e [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**), respectivamente. Novos parâmetros de provedor podem permitir que um CSP seja configurado de maneiras não previstosdas pelos designers do CryptoAPI.<br/>                                                                                                                                                                 |
| Identificadores de algoritmo<br/>                                                                                 | Os recursos de enumeração do [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**) permitem que os aplicativos listem identificadores de algoritmo dinamicamente. Novos algoritmos [*simétricos*](../secgloss/s-gly.md), de [*chave pública*](../secgloss/p-gly.md)e de [*hash*](../secgloss/h-gly.md) podem ser definidos a qualquer momento.<br/> |
| Tipos de par de chaves pública/[*privada*](../secgloss/p-gly.md)<br/> | Embora os novos tipos de pares de chaves possam ser definidos conforme necessário, no momento apenas os pares assinatura e chave de [*troca*](../secgloss/e-gly.md) de chaves são usados.<br/>                                                                                                                                                                                                                                           |
| Tipos de BLOB de chave<br/>                                                                                        | Novos tipos de [*blob*](../secgloss/b-gly.md) de chave podem permitir que chaves de sessão, chaves públicas e pares de chaves públicas/privadas sejam trocados de maneira flexível usando as funções [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) e [**CPImportKey**](https://www.bing.com/search?q=**CPImportKey**) .<br/>                                                                                                                                            |
| Parâmetros de chave<br/>                                                                                        | Os parâmetros de chave são enviados e recuperados usando [**CPSetKeyParam**](https://www.bing.com/search?q=**CPSetKeyParam**) e [**CPGetKeyParam**](https://www.bing.com/search?q=**CPGetKeyParam**). Novos parâmetros de chave podem habilitar o suporte para vários tipos diferentes de chaves.<br/>                                                                                                                                                                                                                         |
| Parâmetros de objeto de hash<br/>                                                                                | Os parâmetros de objeto de hash são enviados e recuperados usando [**CPSetHashParam**](https://www.bing.com/search?q=**CPSetHashParam**) e [**CPGetHashParam**](https://www.bing.com/search?q=**CPGetHashParam**). Novos parâmetros de objeto de hash podem habilitar o suporte para muitos tipos diferentes de [*hashes*](../secgloss/h-gly.md).<br/>                                                                                                                                         |
| Valores de sinalizador<br/>                                                                                           | A maioria das funções CryptoAPI/CryptoSPI tem um parâmetro *dwFlags* . Os novos valores *dwFlags* podem modificar o comportamento das funções conforme necessário.<br/>                                                                                                                                                                                                                                                                                                       |



 

As extensões para CryptoAPI devem ser feitas de maneira responsável. Antes de definir novos parâmetros e tipos de algoritmo, um desenvolvedor CSP deve consultar a Microsoft Corporation para que:

-   As extensões CryptoAPI comuns podem ser identificadas e colocadas no arquivo Wincrypt. h padrão.
-   As colisões de namespace podem ser evitadas.
-   Pode ser determinado se a extensão é necessária ou se uma operação específica pode ser obtida usando a API atual.

> [!Note]  
> Para que um CSP seja compatível com aplicativos desenvolvidos para o provedor Microsoft Base Cryptographic, ele deve dar suporte a todos os itens anteriores, conforme descrito em [funções de criptografia base](cryptography-functions.md) e em [funções de provedor de serviço de criptografia](cryptography-functions.md).

 

 

 
