---
description: 'Se o pacote de instalação enviado com um aplicativo não estiver na raiz do CD-ROM que os clientes recebem, a propriedade MEDIAPACKAGEPATH deverá ser definida na linha de comando para o caminho relativo do aplicativo no CD-ROM. Por exemplo, se o caminho para o pacote na mídia for E: \\ MYPATH \\My.msi, use MEDIAPACKAGEPATH =&\# 0034; \\ MYPATH \\ & \# 0034;. Os administradores podem criar CD-ROMs de um ponto de instalação administrativa. Se o local da raiz da instalação for alterado nos novos CD-ROMs, a propriedade MEDIAPACKAGEPATH deverá ser definida como o novo caminho a ser instalado dessa mídia. Uma fonte com um local no CD-ROM diferente do que está especificado no pacote é inutilizável. No entanto, não é necessário usar essa propriedade ao criar um ponto de instalação administrativa da mídia de envio.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Propriedade MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757388"
---
# <a name="mediapackagepath-property"></a>Propriedade MEDIAPACKAGEPATH

Se o pacote de instalação enviado com um aplicativo não estiver na raiz do CD-ROM que os clientes recebem, a propriedade **MEDIAPACKAGEPATH** deverá ser definida na linha de comando para o caminho relativo do aplicativo no CD-ROM.

Por exemplo, se o caminho para o pacote na mídia for E: \\ MYPATH \\My.msi, então use MEDIAPACKAGEPATH = " \\ MYPATH \\ ".

Os administradores podem criar CD-ROMs de um ponto de instalação administrativa. Se o local da raiz da instalação for alterado nos novos CD-ROMs, a propriedade **MEDIAPACKAGEPATH** deverá ser definida como o novo caminho a ser instalado dessa mídia. Uma fonte com um local no CD-ROM diferente do que está especificado no pacote é inutilizável. No entanto, não é necessário usar essa propriedade ao criar um ponto de instalação administrativa da mídia de envio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




