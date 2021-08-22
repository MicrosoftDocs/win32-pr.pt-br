---
description: O ICE30 valida que a instalação de componentes que contêm o mesmo arquivo nunca instala o arquivo mais de uma vez no mesmo diretório.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba807ec1eb3bde54b1f115e93c531f24414b75e7a293c8ff1b7d7ff1d3abca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528656"
---
# <a name="ice30"></a>ICE30

O ICE30 valida que a instalação de componentes que contêm o mesmo arquivo nunca instala o arquivo mais de uma vez no mesmo diretório.

ICE30 vai para todos os componentes na tabela [Componente](component-table.md) e, em seguida, determina o diretório de destino do componente da [tabela Diretório](directory-table.md). Em seguida, ele verifica qual desses componentes é instalado no mesmo diretório de destino. Por fim, ele usa [a tabela Arquivo](file-table.md) para verificar se nenhum dos arquivos nesses componentes tem o mesmo nome.

ICE30 verifica lfN (nomes de arquivo longos) e SFN (nomes de arquivo curtos).

ICE30 não avalia propriedades na resolução de diretórios porque essas propriedades podem ser alteradas em runtime e alterar o esquema de resolução de diretório. Isso significa que o ICE30 pode detectar colisões de arquivo devido a diretórios com a mesma propriedade em seus caminhos, mas não detecta colisões resultantes de duas propriedades com o mesmo valor.

## <a name="result"></a>Resultado

O ICE30 posta uma mensagem de erro para cada par de componentes que instala o mesmo arquivo no mesmo diretório.

## <a name="example"></a>Exemplo

O exemplo mostrado retorna cada um dos erros a seguir duas vezes.



| Erro ou aviso ICE30                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRO: o arquivo de destino 'README.1st' é instalado em 'TARGETDIR PRODUCT' por dois componentes diferentes em um \\ sistema SFN: 'Component1' e 'Component2'. Isso interrompe a contagem de referência de componente.                                                                                           | Component1 e Component2 têm um arquivo chamado 'READEME.1st'. Ao usar nomes de arquivo curtos, o instalador instala Dir1 e Dir2 no mesmo diretório, TARGETDIR \\ PRODUCT.<br/> ICE30 gera dois erros, um para cada arquivo. Em um ambiente de autor que exibe locais de erro, o [](file-table.md)primeiro erro está na entrada de um arquivo na Tabela de Arquivos e o segundo no local do outro arquivo.<br/> |
| ERRO: a instalação de um componente condicional faria com que o arquivo de destino 'README.1st' fosse instalado em 'TARGETDIR COMMON TOOLS' por dois componentes diferentes em um sistema \\ LFN: 'Component3' e 'Component4'. Isso quebraria a contagem de referência de componente.                      | Component4 tem uma entrada na coluna Condição da tabela [Componente](component-table.md) e Component3 não. Se [**VersionNT**](versionnt.md) for True, Component4 será instalado e haverá uma colisão com o Readme.1st sempre instalado pelo Component3.<br/> ICE30 gera 4 erros, um par para SFN, um para LFN.<br/>                                                                                            |
| AVISO: o arquivo de destino 'README.1st' pode ser instalado em 'TARGETDIR COMMON TOOLS' por dois componentes condicionalizados diferentes em um \\ sistema SFN: 'Component4' e 'Component5'. Se as condições não são mutuamente exclusivas, isso quebrará o sistema de contagem de referência de componente. | Como Component4 e Component5 têm entradas na coluna Condição da tabela [Componente,](component-table.md) essa colisão de arquivo pode não ocorrer. ICE30 só posta um aviso porque as condições devem ser determinadas no momento da instalação.<br/> ICE30 gera 4 avisos, um par para SFN, um para LFN.<br/>                                                                                            |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Diretório | Condição |
|------------|-----------|-----------|
| Component1 | Dir1      |           |
| Component2 | Dir2      |           |
| Component3 | Dir3      |           |
| Component4 | Dir3      | VersionNT |
| Component5 | Dir3      | Version9X |



 

[Tabela de diretórios](directory-table.md)



| Diretório | Diretório \_ pai | Defaultdir                    |
|-----------|-------------------|-------------------------------|
| Sourcedir |                   | Targetdir                     |
| Dir1      | Sourcedir         | Product \| Component1 Product:. |
| Dir2      | Sourcedir         | Produto:.                     |
| Dir3      | Sourcedir         | Common \| Common Tools:         |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ | FileName   |
|-------|-------------|------------|
| Arquivo1 | Component1  | README.1st |
| Arquivo2 | Component2  | README.1st |
| Arquivo3 | Component3  | README.1st |
| Arquivo4 | Component4  | README.1st |
| Arquivo5 | Component5  | README.1st |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




