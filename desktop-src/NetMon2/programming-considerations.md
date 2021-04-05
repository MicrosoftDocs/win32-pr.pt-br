---
description: Este tópico contém informações de programação. A lista a seguir identifica algumas dicas de programação para ajudá-lo a escrever um analisador.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Considerações sobre programação (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213104060f7dd3c6b6dbe56d22044508e0878c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662060"
---
# <a name="programming-considerations-network-monitor"></a>Considerações sobre programação (Monitor de Rede)

Este tópico contém informações de programação. A lista a seguir identifica algumas dicas de programação para ajudá-lo a escrever um analisador.



|                                                 |                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Instalando automaticamente seu analisador                     | Implemente a função [**ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar automaticamente o analisador e atualize os arquivos. ini associados. Se você instalar o analisador manualmente, deverá atualizar todos os arquivos INI associados manualmente.                                                                                                                                                          |
| Propriedades do protocolo de análise                     | Implemente a função [**attachproperties**](attachproperties.md) para analisar as propriedades de protocolo. Evite usar a função [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) ao anexar uma instância de propriedade e usá-la somente para dados alinhados não em byte, ou dados que devem ser decodificados. A anexação de propriedades refere-se ao mapeamento de uma instância de propriedade para um local específico em uma captura. |
| Analisando protocolos divididos entre quadros | Suponha que cada parte do protocolo esteja completa dentro de um quadro e assuma que o usuário chame a ferramenta de União de protocolo para combinar as partes em um protocolo. Não volte em um quadro anterior ao analisar um protocolo e evite tentar reconstruir um protocolo que é dividido entre os quadros.                                                                                              |
| Formatando dados exibidos                       | Chame a função [**FormatPropertyInstance**](formatpropertyinstance.md) para usar o formatador genérico para formatar os dados exibidos no painel de detalhes da interface do usuário do monitor de rede. Evite gravar um formatador personalizado para dados de exibição da interface do usuário. No entanto, você pode chamar um formatador personalizado para criar uma linha de [*propriedade de resumo*](s.md) para o protocolo que você está analisando.            |
| Usando CCAlloc                                   | Use CCAlloc quando desejar que Monitor de Rede aloque dados por captura. Monitor de Rede não especifica a ordem em que os quadros chamam o analisador.                                                                                                                                                                                                                                                |
| Mantendo um analisador sem estado                      | Manter a operação do analisador sem monitoração de estado porque quando Monitor de Rede analisa uma captura, ela não passa os quadros para o analisador em uma ordem específica. Por esse motivo, é recomendável que você não retenha dados globais.                                                                                                                                                                                      |



 

 

 



