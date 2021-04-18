---
description: 'A propriedade time é a hora atual em horas, minutos e segundos como uma cadeia de caracteres de texto literal no formato HH: MM: SS usando um relógio de 24 horas.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Propriedade Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757376"
---
# <a name="time-property"></a>Propriedade Time

A propriedade **time** é a hora atual em horas, minutos e segundos como uma cadeia de caracteres de texto literal no formato hh: mm: SS usando um relógio de 24 horas. Por exemplo, a hora 6:57 é representado por "18:57:00". O formato do valor depende da localidade do usuário e é o formato obtido usando a função [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) com a \_ opção time FORCE24HOURFORMAT \| time \_ NOTIMEMARKER. O valor dessa propriedade é definido pelo Windows Installer e não pelo autor do pacote.

## <a name="remarks"></a>Comentários

Como essa é uma cadeia de caracteres de texto, ela não pode ser usada em expressões condicionais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
