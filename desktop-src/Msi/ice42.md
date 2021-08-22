---
description: ICE42 valida que os servidores InProc não estão vinculados a arquivos EXE na tabela Classe. Ele também valida que somente as classes LocalServer e LocalServer32 têm argumentos e valores DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b913b92d82ad25a9722b289596f6b51940bbade55b5e544ebf636051e21b3ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581066"
---
# <a name="ice42"></a>ICE42

O ICE42 valida que os servidores InProc não estão vinculados a arquivos EXE na [tabela Classe](class-table.md). Ele também valida que somente as classes LocalServer e LocalServer32 têm argumentos e valores DefInProc.

## <a name="result"></a>Resultado

ICE42 postará um erro se houver servidores InProc vinculados a arquivos EXE na tabela Classe.

## <a name="example"></a>Exemplo

ICE42 relataria os erros a seguir para o exemplo mostrado.



| Erro ICE42                                                                                                                             | Descrição                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID '{GUID1}' é um servidor InProc, mas o componente de implementação 'Component1' tem um EXE ('test.exe') como seu KeyFile.                | Há um arquivo executável especificado como um servidor InProc. Os arquivos EXE não podem ser servidores InProc.                                                                                                                            |
| CLSID '{GUID1}' no contexto 'InProcServer32' tem um argumento . Somente contextos LocalServer podem ter argumentos.                              | Para corrigir esse erro, remova o argumento .                                                                                                                                                                                   |
| CLSID '{GUID1}' no contexto 'InProcServer32' especifica um valor InProc padrão. Somente os contextos LocalServer podem ter valores InProc padrão. | Há um objeto com um valor InProc padrão que não é um objeto que opera nos contextos LocalServer ou LocalServer32. Para corrigir esse erro, remova o valor DeflnProc ou altere o contexto da classe .<br/> |



 

[Tabela de Classe](class-table.md) (parcial)



| CLSID   | Contexto        | Componente\_ | DefInProcHandler | Argumento |
|---------|----------------|-------------|------------------|----------|
| {GUID1} | Inprocserver32 | Component1  | InProcServer     | Arg      |



 

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

 

 




