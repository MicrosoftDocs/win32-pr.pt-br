---
title: Terminologia da estrutura biométrica
description: Os termos a seguir são usados em toda a documentação da API do Windows Biometric Framework.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f150a30915a44dbd59a5a703577e79dc48933f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636884"
---
# <a name="biometric-framework-terminology"></a>Terminologia da estrutura biométrica

Os termos a seguir são usados em toda a documentação da API do Windows Biometric Framework.



| Termo                                                 | Definição                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Biometric Framework (WBF)<br/>         | Uma arquitetura de estrutura no Windows que fornece uma interface de gerenciamento consistente e experiência do usuário para dispositivos biométricos.<br/>                                                                                                                         |
| Serviço de Biometria do Windows<br/>                 | Um serviço privilegiado que gerencia todos os dispositivos biométricos usando drivers de dispositivo compatíveis com WBDI (Windows biometria driver interface).<br/>                                                                                                                   |
| Interface de driver biométrico do Windows<br/>        | Um padrão de interface para drivers que gerenciam sensores de impressão digital.<br/>                                                                                                                                                                                     |
| Provedor de serviços biométricos do Windows (WBSP)<br/> | Um componente do serviço biométrico do Windows que gerencia uma categoria específica de tecnologia biométrica, como um leitor de impressão digital. WBSPs são incorporados ao serviço biométrico do Windows. Eles não são plug-ins e BSPs de terceiros não têm suporte. <br/> |
| Fator biométrico<br/>                          | Uma característica pessoal que pode ser medida e usada para identificação. Os exemplos incluem impressões digitais e a geometria de mão.<br/>                                                                                                                           |
| Sub-fator biométrico<br/>                      | Uma característica de qualificação que pode ser usada para definir ainda mais um fator biométrico. Por exemplo, para identificar completamente uma impressão digital (fator de biometria), é necessário especificar a qual dedo a impressão veio (subfator de biometria).<br/>             |
| Exemplo biométrica<br/>                          | Os dados resultantes da medição de uma única característica de um único indivíduo, por exemplo, a imagem de uma impressão digital.<br/>                                                                                                              |
| Modelo biométrico<br/>                        | Uma média estatística gerada pela coleta de várias amostras biométricas de uma única característica para um único indivíduo. Um modelo geralmente contém somente os recursos que são necessários para determinar se uma nova amostra é correspondente.<br/>             |
| Unidade biométrica<br/>                            | Um objeto de software que representa um dispositivo biométrico e pode ser usado para capturar e processar amostras biométricas e criar, salvar e combinar modelos biométricos.<br/>                                                                                         |
| Adaptador do sensor<br/>                            | Um componente de plug-in de unidade biométrica que fornece uma interface padrão para configurar o sensor, capturar amostras e controlar o fluxo de dados biométricos para o adaptador do mecanismo.<br/>                                                                 |
| Adaptador do mecanismo<br/>                            | Um componente de plug-in de unidade biométrica que processa um exemplo normalizando dados, extraindo recursos e combinando dados de exemplo para modelos existentes.<br/>                                                                                                   |
| Adaptador de armazenamento<br/>                           | Um componente de plug-in de unidade biométrica que armazena, gerencia e recupera modelos.<br/>                                                                                                                                                                      |
| Registro de informações biométricas (BIR)<br/>        | Uma estrutura de dados que contém informações de biométricas brutas ou processadas.<br/>                                                                                                                                                                                 |
| Pool de sensores<br/>                               | Uma coleção de unidades biométricas que compartilham uma política de gerenciamento comum.<br/>                                                                                                                                                                                 |
| Testes de vida<br/>                          | Um processo que verifica se um exemplo biométrico não está sendo falsificado ou reproduzido a partir de um exemplo que foi coletado anteriormente.<br/>                                                                                                                          |



 

 

 





