---
description: A propriedade INSTALLLEVEL é o nível inicial no qual os recursos são selecionados &\# 0034; em&\# 0034; para instalação por padrão.
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

A propriedade **INSTALLLEVEL** é o nível inicial no qual os recursos são selecionados "ativados" para instalação por padrão. Um recurso será instalado somente se o valor no campo nível da tabela de [recursos](feature-table.md) for menor ou igual ao valor de INSTALLLEVEL atual. O nível de instalação para qualquer instalação é especificado pela propriedade **INSTALLLEVEL** e pode ser um integral de 1 a 32.767. Para obter mais informações sobre os níveis de instalação, consulte [tabela de recursos](feature-table.md).

## <a name="default-value"></a>Valor padrão

Se nenhum valor for especificado, o nível de instalação padrão será 1.

## <a name="remarks"></a>Comentários

O nível de instalação especificado pela propriedade **INSTALLLEVEL** pode ser substituído pelas seguintes propriedades:

-   [**ADDLOCAL**](addlocal.md)
-   [**Addsource**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**EXCLU**](remove.md)
-   [**Install**](reinstall.md)
-   [**ANUNCI**](advertise.md)

Por exemplo, a configuração de ADDLOCAL = ALL instala todos os recursos localmente, independentemente do valor da propriedade **INSTALLLEVEL** . Se o valor da coluna nível na tabela de [recursos](feature-table.md) for 0, esse recurso não será instalado e não exibido na interface do usuário.

Um administrador pode desabilitar permanentemente um recurso aplicando uma transformação de personalização que define um 0 na coluna nível para esse recurso. O aplicativo da transformação personalização impede a instalação e a exibição do recurso, mesmo que o usuário selecione uma instalação completa usando a interface do usuário ou definindo ADDLOCAL como ALL na linha de comando. Consulte [um exemplo de transformação personalização](a-customization-transform-example.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




