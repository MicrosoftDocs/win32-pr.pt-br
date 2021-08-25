---
description: 'Se o envio do pacote de instalação com um aplicativo não estiver na raiz do CD-ROM que os clientes recebem, a propriedade MEDIAPACKAGEPATH deverá ser definida na linha de comando para o caminho relativo do aplicativo no CD-ROM. Por exemplo, se o caminho para o pacote na mídia for E: \\ MyPath \\My.msi, use MEDIAPACKAGEPATH=&\# 0034; \\ MyPath \\ & \# 0034;. Os administradores podem criar CD-ROMs de um ponto de instalação administrativa. Se o local da raiz da instalação for alterado nos novos CD-ROMs, a propriedade MEDIAPACKAGEPATH deverá ser definida como o novo caminho a ser instalado por meio dessa mídia. Uma origem com um local no CD-ROM diferente do especificado no pacote é inutilizável. No entanto, não é necessário usar essa propriedade ao criar um ponto de instalação administrativa da mídia de envio.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Propriedade MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140afc253e27b3c861f941e88b55f84ad49f43984fcc3a5aaf82d06fe414e6a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926876"
---
# <a name="mediapackagepath-property"></a>Propriedade MEDIAPACKAGEPATH

Se o envio do pacote de instalação com um aplicativo não estiver na raiz do CD-ROM que os clientes recebem, a propriedade **MEDIAPACKAGEPATH** deverá ser definida na linha de comando para o caminho relativo do aplicativo no CD-ROM.

Por exemplo, se o caminho para o pacote na mídia for E: \\ MyPath \\My.msi, use MEDIAPACKAGEPATH=" \\ MyPath \\ ".

Os administradores podem criar CD-ROMs de um ponto de instalação administrativa. Se o local da raiz da instalação for alterado nos novos CD-ROMs, a propriedade **MEDIAPACKAGEPATH** deverá ser definida como o novo caminho a ser instalado por meio dessa mídia. Uma origem com um local no CD-ROM diferente do especificado no pacote é inutilizável. No entanto, não é necessário usar essa propriedade ao criar um ponto de instalação administrativa da mídia de envio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




