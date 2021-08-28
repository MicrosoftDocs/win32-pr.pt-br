---
description: Consulte uma lista de sinalizadores de funcionalidade do driver D3DCAPS2. Inclui as definições, valores e descrições com links para APIs.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adada1f5e38247482af38cd335c6fd719cf9a603
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627702"
---
# <a name="d3dcaps2"></a>D3DCAPS2

Sinalizadores de funcionalidade do driver.



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
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x4000000L</td>
<td>O driver é capaz de gerar mipmaps automaticamente. Para obter mais informações, <a href="automatic-generation-of-mipmaps.md">consulte Geração automática de Mipmaps (Direct3D 9)</a>.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>O sistema tem um calibrador instalado que pode ajustar automaticamente a rampa gama para que o resultado seja idêntico em todos os sistemas que têm um calibrador. Para invocar o calibrador ao definir novos níveis gama, use o sinalizador D3DSGR_CALIBRATE ao chamar <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>. A calibração de rampas gama incorre em alguma sobrecarga de processamento e não deve ser usada com frequência.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x8000000L</td>
<td>O dispositivo pode criar recursos compartilháveis. Métodos que criam recursos podem definir valores não NULL para seus <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>parâmetros pSharedHandle.</strong></a> 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANMANAGERESOURCE</td>
<td>0x10000000L</td>
<td>O driver é capaz de gerenciar recursos. Nesses drivers, D3DPOOL_MANAGED recursos serão gerenciados pelo driver. Para que o Direct3D substitua o driver para que o Direct3D gerencie recursos, use o sinalizador D3DCREATE_DISABLE_DRIVER_MANAGEMENT ao chamar <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000L</td>
<td>O driver dá suporte a texturas dinâmicas.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000L</td>
<td>O driver dá suporte ao ajuste dinâmico de rampa gama no modo de tela inteira.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000L</td>
<td>Reservado; não usado.</td>
</tr>
</tbody>
</table>



 

Essas constantes são usadas pelo membro D3CAPS2 [**de D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informações constantes



|  Requisito                        | Valor           |
|--------------------------|------------|
| parâmetro                   | d3d9caps.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
