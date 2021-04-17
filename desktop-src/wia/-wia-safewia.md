---
description: O objeto SafeWia é um &\# 0034; seguro para scripts&\# 0034; ponto de entrada para a funcionalidade de script da aquisição de imagem do Windows (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Objeto SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812013"
---
# <a name="safewia-object"></a>Objeto SafeWia

O objeto **SafeWia** é um ponto de entrada "seguro para scripts" para toda a funcionalidade de script da aquisição de imagem do Windows (WIA). Qualquer aplicativo que usa o modelo de script WIA deve criar um objeto **SafeWia** ou [**WIA**](-wia-wia.md) . Use esse objeto para enumerar e criar dispositivos e para receber notificações de eventos de hardware.

## <a name="members"></a>Membros

O objeto **SafeWia** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SafeWia** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Criada**](-wia-iwia-create.md) | O método [**Create**](-wia-iwia-create.md) do objeto [**WIA**](-wia-wia.md) faz uma conexão com o dispositivo WIA especificado e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SafeWia** tem essas propriedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriedade</th>
<th style="text-align: left;">Tipo de acesso</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Coleção de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos os dispositivos instalados no computador. Somente leitura. <br/>
<blockquote>
[!Note]<br />
Esta coleção é baseada em 0.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |
| IID<br/>                      | \_SAFEWIA CLSID<br/>                                                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WIA**](-wia-wia.md)
</dt> </dl>

 

 




