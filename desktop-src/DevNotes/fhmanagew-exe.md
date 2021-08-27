---
description: O FhManagew.exe exclui versões de arquivo que excedem uma idade especificada do dispositivo de destino Histórico de Arquivos atribuído no momento.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2570da9b2b874b723b28917028fab3c58ecdf772
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481512"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

O FhManagew.exe exclui versões de arquivo que excedem uma idade especificada do dispositivo de destino Histórico de Arquivos atribuído no momento.

Este programa está disponível em Windows 8 e Windows Server 2012 e posterior.

Para executar esse programa, vá para o menu **Iniciar,** clique **em Executar** e digite o comando a seguir.

**FhManagew.exe -cleanup** *age*




| Parâmetro | Descrição | 
|-----------|-------------|
| <span id="age"></span><span id="AGE"></span><em>Idade</em><br /> | Esse parâmetro especifica a idade mínima, em dias, das versões de arquivo que podem ser excluídas. Uma versão do arquivo será excluída se ambas as seguintes condições são verdadeiras:<br /><ul><li>A versão do arquivo é mais antiga do que a idade especificada.</li><li>O arquivo não está mais incluído no escopo de proteção ou há uma versão mais recente do mesmo arquivo no dispositivo de destino.</li></ul>Se o <em>parâmetro age</em> estiver definido como zero, todas as versões de arquivo serão excluídas, exceto pela versão mais recente de cada arquivo que está presente no escopo de proteção no momento.<br /> | 




 

Para suprimir toda a saída desse programa, use a opção de linha de comando **-quiet** da seguinte forma.

**FhManagew.exe -cleanup** *age* **-quiet**

## <a name="examples"></a>Exemplos



| Exemplo                                                                                                                                                                                                      | Descrição                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**<br/>                                 | Exclua todas as versões de arquivo com mais de um mês.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**<br/> | Exclua todas as versões de arquivo com mais de um ano e suprime todas as saídas.<br/> |



 

 

 




