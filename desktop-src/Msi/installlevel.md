---
description: A propriedade INSTALLLEVEL é o nível inicial no qual os recursos são selecionados &\# 0034;ON&0034; para instalação por \# padrão.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Propriedade INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e349e8d92a2c480866b04a1ca57885ffa1cdb230d8346b357318fa239ead72a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629955"
---
# <a name="installlevel-property"></a>Propriedade INSTALLLEVEL

A **propriedade INSTALLLEVEL** é o nível inicial no qual os recursos são selecionados como "ON" para instalação por padrão. Um recurso será instalado somente se o valor [](feature-table.md) no campo Nível da tabela Recurso for menor ou igual ao valor INSTALLLEVEL atual. O nível de instalação para qualquer instalação é especificado pela **propriedade INSTALLLEVEL** e pode ser um integral de 1 a 32.767. Para mais discussão sobre níveis de instalação, consulte [Tabela de recursos](feature-table.md).

## <a name="default-value"></a>Valor padrão

Se nenhum valor for especificado, o nível de instalação será padrão como 1.

## <a name="remarks"></a>Comentários

O nível de instalação especificado pela **propriedade INSTALLLEVEL** pode ser substituído pelas seguintes propriedades:

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**Remover**](remove.md)
-   [**Reinstalar**](reinstall.md)
-   [**Anunciar**](advertise.md)

Por exemplo, definir ADDLOCAL=ALL instala todos os recursos localmente, independentemente do valor da **propriedade INSTALLLEVEL.** Se o valor da coluna [](feature-table.md) Nível na tabela Recurso for 0, esse recurso não será instalado e não será exibido na interface do usuário.

Um administrador pode desabilitar permanentemente um recurso aplicando uma transformação de personalização que define um 0 na coluna Nível para esse recurso. A aplicação da transformação de personalização impede a instalação e a exibição do recurso mesmo que o usuário selecione uma instalação completa usando a interface do usuário ou definindo ADDLOCAL como ALL na linha de comando. Consulte [um exemplo de transformação de personalização](a-customization-transform-example.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão do Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




