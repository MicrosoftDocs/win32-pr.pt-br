---
description: Descreve os arquivos de entrada consumidos por WsdCodeGen e os arquivos de saída gerados pelo WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Sobre o WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010814"
---
# <a name="about-wsdcodegen"></a>Sobre o WsdCodeGen

O WsdCodeGen usa um arquivo de configuração XML para determinar o local dos metadados do serviço. O arquivo de configuração também é usado para definir nomes de interface, GUIDs de interface, nomes de classe, nomes de método e outros identificadores. Para obter mais informações sobre esse arquivo, consulte [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).

O WsdCodeGen requer dois tipos de arquivos de entrada: um arquivo de configuração XML e um ou mais arquivos de descrição de serviço (arquivos WSDL e/ou XSD). O WsdCodeGen processa esses arquivos de entrada e gera dois tipos de arquivos de saída: Arquivos de interface e arquivos de cabeçalho/origem.

## <a name="input-files"></a>Arquivos de entrada



| Tipo                      | Descrição                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arquivo de configuração        | Um arquivo XML que indica o local dos metadados do serviço e define nomes de interface, GUIDs de interface, nomes de classe, nomes de método e outros identificadores. |
| Arquivos de descrição de serviço | Um ou mais arquivos WSDL ou XSD que descrevem os serviços a serem implementados no dispositivo.                                                                           |



 

## <a name="output-files"></a>Arquivos de saída



| Tipo                        | Descrição                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arquivos de interface             | Um arquivo IDL (linguagem de definição de interface) que pode ser usado com o compilador MIDL para produzir um arquivo de cabeçalho de interface. Os clientes WSDAPI e os serviços WSDAPI podem usar esse arquivo de interface.                                                                                                                                                           |
| Arquivos de cabeçalho e origem do C++ | Arquivos C++ que descrevem o contrato de mensagem, o namespace e as informações de tipo. Eles podem conter código de proxy e/ou código stub. O código do proxy implementa a interface de um serviço e traduz as chamadas de método de serviço em operações WSDAPI que fazem solicitações de serviço. O código stub converte solicitações de serviço WSDAPI em código que chama métodos de serviço. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços Web no gerador de código de dispositivos](web-services-for-devices-code-generator.md)
</dt> <dt>

[Usando WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 



