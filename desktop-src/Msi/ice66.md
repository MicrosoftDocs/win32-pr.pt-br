---
description: O ICE66 usa as tabelas no banco de dados para determinar qual esquema seu banco de dados deve usar.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023450a451a412c47c21904ab96a13e4513c71f8327966dffa5b657b1b65bb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787396"
---
# <a name="ice66"></a>ICE66

O ICE66 usa as tabelas no banco de dados para determinar qual esquema seu banco de dados deve usar.

algumas funcionalidades só poderão ser disponibilizadas se o pacote estiver instalado em um sistema com uma versão atual do Windows Installer.

## <a name="result"></a>Resultado

ICE66 posta um aviso se o seu banco de dados estiver usando o esquema incorreto.

## <a name="example"></a>Exemplo

ICE66 relata o seguinte aviso para o exemplo mostrado.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

esse aviso poderá ser ignorado se você quiser que o pacote seja instalado usando uma versão de Windows Installer atual. Por exemplo, se você quiser que o pacote seja instalado somente na versão 2,0 ou posterior, altere o esquema do pacote (PID \_ PageCount) para 200.

[Tabela IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ compartilhado | Aplicativo de componente \_ |
|-------------------|------------------------|
| Component1        | Component2             |



 

[Fluxo de informações de resumo](summary-information-stream.md)



| PIDt           | Valor |
|----------------|-------|
| DTI \_ PageCount | 100   |



 

## <a name="table-used-during-execution"></a>Tabela usada durante a execução:

[\_Tabela de colunas](-columns-table.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



