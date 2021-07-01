---
description: Este tópico contém informações de programação. A lista a seguir identifica algumas dicas de programação para ajudá-lo a escrever um analisador.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Considerações sobre programação (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2deb53a27d8abda4f45663b65fb922600a5b5386
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120221"
---
# <a name="programming-considerations-network-monitor"></a>Considerações sobre programação (Monitor de Rede)

Este tópico contém informações de programação. A lista a seguir identifica algumas dicas de programação para ajudá-lo a escrever um analisador.



| Dica                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Instalando automaticamente o analisador                     | Implemente [**a função ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar automaticamente o analisador e atualizar os arquivos INI associados. Se você instalar o analisador manualmente, deverá atualizar todos os arquivos INI associados manualmente.                                                                                                                                                          |
| Analisar propriedades do protocolo                     | Implemente [**a função AttachProperties**](attachproperties.md) para analisar as propriedades do protocolo. Evite usar a [**função AttachPropertyInstanceEx**](attachpropertyinstanceex.md) ao anexar uma instância de propriedade e use-a apenas para dados não alinhados a byte ou dados que devem ser decodificados. Anexar propriedades refere-se ao mapeamento de uma instância de propriedade para um local específico em uma captura. |
| Analisar protocolos que são divididos entre quadros | Suponha que cada parte do protocolo seja concluída em um quadro e suponha que o usuário chama a ferramenta Protocol Coalesce para combinar as partes em um protocolo. Não volte para um quadro anterior ao analisar um protocolo e evite tentar reconstruir um protocolo dividido entre quadros.                                                                                              |
| Formatação de dados exibidos                       | Chame a [**função FormatPropertyInstance**](formatpropertyinstance.md) para usar o formatante genérico para formatar os dados exibidos no painel de detalhes da interface Monitor de Rede interface do usuário. Evite escrever um formatante personalizado para dados de exibição da interface do usuário. No entanto, você pode chamar um formatante personalizado para criar uma linha de [*propriedade*](s.md) de resumo para o protocolo que está sendo analisado.            |
| Usando CCAlloc                                   | Use CCAlloc quando quiser Monitor de Rede alocar dados por captura. Monitor de Rede não especifica a ordem em que os quadros chamam o analisador.                                                                                                                                                                                                                                                |
| Mantendo um analisador sem estado                      | Mantenha a operação do analisador sem estado porque quando Monitor de Rede uma captura, ela não passa os quadros para o analisador em uma ordem específica. Por esse motivo, é recomendável que você não mantenha os dados globais.                                                                                                                                                                                      |



 

 

 



