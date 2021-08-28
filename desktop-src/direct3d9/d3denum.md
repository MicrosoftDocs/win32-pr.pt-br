---
description: Sinalizador de funcionalidade do driver.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb3ed10a4a12602e8586bbd0e941641287346a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627992"
---
# <a name="d3denum"></a>D3DENUM

Sinalizador de funcionalidade do driver.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Valor</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>Teste de driver do WHQL (Hardware Quality Labs) do Microsoft Windows. Esse é um teste demorado que exige uma penalidade de tempo de um segundo ou dois segundos. Essa constante é usada pelo membro WHQLLevel do <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> D3DENUM_WHQL_LEVEL foi preterido para Direct3D9Ex em execução no Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (ou sistema operacional mais atual). Qualquer um desses sistemas operacionais retorna 1 para o nível WHQL sem verificar o status do driver. <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor           |
|--------------------------|------------|
| parâmetro                   | d3d9.h     |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




