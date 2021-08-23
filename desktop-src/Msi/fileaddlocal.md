---
description: O valor da propriedade FILEADDLOCAL denota uma lista de chaves de arquivo delimitadas por vírgulas que devem ser instaladas para serem executados da mídia de origem local.
ms.assetid: 89ae876e-53f0-4c1d-ba16-7513af79ee5e
title: Propriedade FILEADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c764fa89480cf4f37e19a4f6a10ee354a07bfe18f9fbc203ea0db4410f7bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946986"
---
# <a name="fileaddlocal-property"></a>Propriedade FILEADDLOCAL

O valor da **propriedade FILEADDLOCAL** denota uma lista de chaves de arquivo delimitadas por vírgulas que devem ser instaladas para serem executados da mídia de origem local. Para cada chave de arquivo na lista, o instalador determina o componente que controla esse arquivo e examina todos os recursos vinculados a esse componente pela tabela [FeatureComponents](featurecomponents-table.md) e instala o recurso que requer a menor quantidade de espaço em disco. As chaves de arquivo na lista devem estar presentes na coluna Arquivo da [tabela](file-table.md) Arquivo.

## <a name="remarks"></a>Comentários

Observe que os nomes de chave de arquivo são sensíveis a minúsculas. Observe também que, se o sinalizador de bit LocalOnly estiver definido na coluna Atributos da tabela Componente de um componente, o componente será instalado para ser executado localmente. [](component-table.md)

O instalador sempre avalia as propriedades a seguir na ordem a seguir.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Remover**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. **FILEADDLOCAL**
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por exemplo, se a linha de comando especificar: ADDLOCAL=ALL, ADDSOURCE = MyFeature, todos os recursos serão definidos primeiro como run-local e, em seguida, MyFeature será definido como run-from-source. Se a linha de comando for: ADDSOURCE=ALL, ADDLOCAL=MyFeature, primeiro MyFeature será definido como run-local e, em seguida, quando ADDSOURCE=ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para run-from-source.

O instalador define a propriedade [**Pré-selecionada**](preselected.md) como um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




