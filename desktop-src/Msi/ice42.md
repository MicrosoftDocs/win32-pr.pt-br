---
description: ICE42 valida que os servidores InProc não estão vinculados a arquivos EXE na tabela de classes. Ele também valida que somente as classes LocalServer e LocalServer32 têm argumentos e valores DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752651"
---
# <a name="ice42"></a>ICE42

ICE42 valida que os servidores InProc não estão vinculados a arquivos EXE na [tabela de classes](class-table.md). Ele também valida que somente as classes LocalServer e LocalServer32 têm argumentos e valores DefInProc.

## <a name="result"></a>Resultado

ICE42 posta um erro se houver servidores InProc vinculados a arquivos EXE na tabela de classes.

## <a name="example"></a>Exemplo

ICE42 relataria os erros a seguir para o exemplo mostrado.



| Erro de ICE42                                                                                                                             | Descrição                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID ' {GUID1} ' é um servidor InProc, mas o componente de implementação ' Component1 ' tem um EXE (' test.exe ') como KeyFile.                | Há um arquivo executável especificado como um servidor InProc. Os arquivos EXE não podem ser servidores InProc.                                                                                                                            |
| O CLSID ' {GUID1} ' no contexto ' InProcServer32 ' tem um argumento. Somente contextos de LocalServer podem ter argumentos.                              | Para corrigir esse erro, remova o argumento.                                                                                                                                                                                   |
| CLSID ' {GUID1} ' no contexto ' InProcServer32 ' especifica um valor de InProc padrão. Somente contextos de LocalServer podem ter valores de InProc padrão. | Há um objeto com um valor de InProc padrão que não é um objeto operando nos contextos LocalServer ou LocalServer32. Para corrigir esse erro, remova o valor DeflnProc ou altere o contexto da classe.<br/> |



 

[Tabela de classes](class-table.md) (parcial)



| CLSID   | Contexto        | Componente\_ | DefInProcHandler | Argumento |
|---------|----------------|-------------|------------------|----------|
| GUID1 | InProcServer32 | Component1  | InProcServer     | ARG      |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | KeyPath |
|------------|---------|
| Component1 | Arquivo1   |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Nome de arquivo |
|-------|----------|
| Arquivo1 | test.exe |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




