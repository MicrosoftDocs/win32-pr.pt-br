---
description: ICE30 valida que a instalação de componentes que contém o mesmo arquivo nunca instala o arquivo mais de uma vez no mesmo diretório.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769317"
---
# <a name="ice30"></a>ICE30

ICE30 valida que a instalação de componentes que contém o mesmo arquivo nunca instala o arquivo mais de uma vez no mesmo diretório.

ICE30 vai para todos os componentes na [tabela de componentes](component-table.md) e determina o diretório de destino do componente da [tabela de diretórios](directory-table.md). Em seguida, ele verifica para ver quais desses componentes são instalados no mesmo diretório de destino. Por fim, ele usa a [tabela de arquivos](file-table.md) para verificar se nenhum dos arquivos nesses componentes tem o mesmo nome.

ICE30 verifica nomes de arquivo longos (LFN) e nomes de arquivo curtos (SFN).

ICE30 não avalia as propriedades na resolução de diretórios porque essas propriedades podem ser alteradas em tempo de execução e alterar o esquema de resolução de diretório. Isso significa que o ICE30 pode detectar colisões de arquivo devido a diretórios com a mesma propriedade em seus caminhos, mas não detecta colisões resultantes de duas propriedades com o mesmo valor.

## <a name="result"></a>Resultado

O ICE30 posta uma mensagem de erro para cada par de componentes que instala o mesmo arquivo no mesmo diretório.

## <a name="example"></a>Exemplo

O exemplo mostrado retorna cada um dos seguintes erros duas vezes.



| Erro ou aviso do ICE30                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRO: o arquivo de destino ' README. 1o ' está instalado em ' TARGETDIR \\ Product ' por dois componentes diferentes em um sistema SFN: ' Component1 ' e ' Component2 '. Essa contagem de referência de componente de quebras.                                                                                           | Component1 e Component2 têm um arquivo chamado ' READEME. 1o '. Ao usar nomes de arquivo curtos, o instalador instala dir1 e dir2 no mesmo diretório, produto TARGETDIR \\ .<br/> ICE30 gera dois erros, um para cada arquivo. Em um ambiente de criação que exibe locais de erro, o primeiro erro está na entrada de um arquivo na [tabela de arquivos](file-table.md)e o segundo no local do outro arquivo.<br/> |
| ERRO: a instalação de um componente condicional faria com que o arquivo de destino ' README. 1o ' fosse instalado em ' TARGETDIR \\ Common Tools ' por dois componentes diferentes em um sistema LFN: ' Component3 ' e ' Component4 '. Isso interromperia a contagem de referências de componentes.                      | Component4 tem uma entrada na coluna Condition da [tabela Component](component-table.md) e Component3 não. Se [**VersionNT**](versionnt.md) for true, Component4 será instalado e haverá uma colisão com o README. 1o sempre instalado pelo Component3.<br/> O ICE30 gera 4 erros, um par para SFN, um para LFN.<br/>                                                                                            |
| Aviso: o arquivo de destino ' README. 1o ' pode ser instalado em ' TARGETDIR \\ Common Tools ' por dois componentes condicionais diferentes em um sistema SFN: ' Component4 ' e ' Component5 '. Se as condições não forem mutuamente exclusivas, isso interromperá o sistema de contagem de referência do componente. | Como Component4 e Component5 têm entradas na coluna condição da [tabela de componentes](component-table.md) , essa colisão de arquivo pode não ocorrer. O ICE30 posta apenas um aviso porque as condições devem ser determinadas no momento da instalação.<br/> O ICE30 gera 4 avisos, um par para SFN, um para LFN.<br/>                                                                                            |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Diretório | Condição |
|------------|-----------|-----------|
| Component1 | Dir1      |           |
| Component2 | Dir2      |           |
| Component3 | Dir3      |           |
| Component4 | Dir3      | VersionNT |
| Component5 | Dir3      | Version9X |



 

[Tabela de diretórios](directory-table.md)



| Diretório | \_Diretório pai | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | TARGETDIR                     |
| Dir1      | SOURCEDIR         | Produto \| Component1 produto:. |
| Dir2      | SOURCEDIR         | Produto:.                     |
| Dir3      | SOURCEDIR         | \|Ferramentas comuns comuns:         |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ | FileName   |
|-------|-------------|------------|
| Arquivo1 | Component1  | LEIAme. 1º |
| Arquivo2 | Component2  | LEIAme. 1º |
| Arquivo3 | Component3  | LEIAme. 1º |
| Arquivo4 | Component4  | LEIAme. 1º |
| Arquivo5 | Component5  | LEIAme. 1º |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




