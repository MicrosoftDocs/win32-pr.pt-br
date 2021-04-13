---
description: O programa de FhManagew.exe exclui versões de arquivo que excedem uma idade especificada do dispositivo de destino do histórico de arquivos atribuído no momento.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457005"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

O programa de FhManagew.exe exclui versões de arquivo que excedem uma idade especificada do dispositivo de destino do histórico de arquivos atribuído no momento.

Este programa está disponível no Windows 8 e no Windows Server 2012 e posterior.

Para executar este programa, vá para o menu **Iniciar** , clique em **executar** e digite o comando a seguir.

**FhManagew.exe-idade de limpeza** 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parâmetro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="age"></span><span id="AGE"></span><em>idade</em><br/></td>
<td>Esse parâmetro especifica a idade mínima, em dias, das versões de arquivo que podem ser excluídas. Uma versão de arquivo será excluída se as duas condições a seguir forem verdadeiras:<br/>
<ul>
<li>A versão do arquivo é mais antiga que a idade especificada.</li>
<li>O arquivo não está mais incluído no escopo de proteção ou há uma versão mais recente do mesmo arquivo no dispositivo de destino.</li>
</ul>
Se o parâmetro <em>age</em> for definido como zero, todas as versões de arquivo serão excluídas, exceto para a versão mais recente de cada arquivo presente atualmente no escopo de proteção.<br/></td>
</tr>
</tbody>
</table>



 

Para suprimir toda a saída deste programa, use a opção de linha de comando **-Quiet** da seguinte maneira.

 *Idade* da limpeza **deFhManagew.exe-Quiet**

## <a name="examples"></a>Exemplos



| Exemplo                                                                                                                                                                                                      | Descrição                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-limpeza 30**<br/>                                 | Exclua todas as versões de arquivo com mais de um mês.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-limpeza 365-Quiet**<br/> | Exclua todas as versões de arquivo com mais de um ano e omita todas as saídas.<br/> |



 

 

 




