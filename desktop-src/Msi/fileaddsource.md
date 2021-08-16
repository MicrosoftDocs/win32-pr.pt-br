---
description: O valor da propriedade FILEADDSOURCE denota uma lista de chaves de arquivo delimitadas por vírgulas que devem ser instaladas para serem executadas a partir da mídia de origem.
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: Propriedade FILEADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7678c42e683b70fc61e563c57ee234c523078bcdd737bf8f28bc2c05302fbb43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636558"
---
# <a name="fileaddsource-property"></a>Propriedade FILEADDSOURCE

O valor da propriedade **FILEADDSOURCE** denota uma lista de chaves de arquivo delimitadas por vírgulas que devem ser instaladas para serem executadas a partir da mídia de origem. Para cada chave de arquivo na lista, o instalador determina o componente que controla esse arquivo e, em seguida, examina todos os recursos vinculados a esse componente pela tabela [FeatureComponents](featurecomponents-table.md) e instala o recurso que requer a quantidade mínima de espaço em disco. As chaves de arquivo na lista devem estar presentes na coluna arquivo da tabela de [arquivos](file-table.md) .

## <a name="remarks"></a>Comentários

Observe que os nomes de chave de arquivo diferenciam maiúsculas de minúsculas. Observe também que, se o sinalizador de bit LocalOnly estiver definido na coluna atributos da tabela de [componentes](component-table.md) de um componente, o componente será instalado para ser executado localmente.

O instalador sempre avalia as propriedades a seguir na seguinte ordem.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**EXCLU**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Install**](reinstall.md)
6.  [**ANUNCI**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. **FILEADDSOURCE**
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por exemplo, se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source. Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local e, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para execução-da-source.

O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




