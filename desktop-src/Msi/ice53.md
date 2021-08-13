---
description: O ICE53 verifica se há entradas na tabela do Registro que escrevem informações privadas do instalador ou valores de política no registro do sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d1e661eb832439a9b4fde423e005dc4b3a0c3ca9b266045c0ddd04daa63f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635127"
---
# <a name="ice53"></a>ICE53

O ICE53 verifica se há entradas na tabela do Registro que escrevem informações privadas do instalador ou valores de política no registro do sistema.

## <a name="result"></a>Result

ICE53 postará um aviso se a tabela do Registro especificar a escrita de informações internas ou de política no Registro.

## <a name="example"></a>Exemplo

ICE53 posta o seguinte aviso para o exemplo mostrado.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Tabela do Registro](registry-table.md) (parcial)



| Registro             | Root         | Chave                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **Software** \\ **Políticas** \\ **Microsoft** \\ **Windows** \\ **Instalador** \\ **DisableRollback**<br/> |



 

A linha da tabela do Registro 'Registry1' grava um valor de política do sistema no Registro que afeta a instalação de todos os pacotes. Dependendo do pacote, pode ser possível desabilitar a reação somente para este pacote definindo a propriedade [**DISABLEROLLBACK**](-disablerollback.md) na [tabela Property](property-table.md). Consulte [Instalação de reação](rollback-installation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




