---
description: Ocorre quando um novo relatório de latitude/longitude é gerado.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Evento NewLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789636"
---
# <a name="newlatlongreport-event"></a>Evento NewLatLongReport

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Ocorre quando um novo relatório de latitude/longitude é gerado.

## <a name="syntax"></a>Sintaxe


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newReport* 
</dt> <dd>

O novo objeto [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse evento, consulte [escutando eventos de relatório do LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

