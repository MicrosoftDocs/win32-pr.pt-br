---
description: O valor da propriedade REMOVE é uma lista de recursos delimitados por vírgulas que devem ser removidas.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: propriedade REMOVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747323"
---
# <a name="remove-property"></a>propriedade REMOVE

O valor da propriedade **Remove** é uma lista de recursos delimitados por vírgulas que devem ser removidas. Os recursos devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md). Observe que se você usar REMOVE = ALL na linha de comando, o instalador removerá todos os recursos que têm um nível de instalação maior que 0. Nesse caso, o instalador não remove os recursos que têm um nível de instalação de 0. Para obter mais informações sobre o nível de instalação dos recursos, consulte [tabela de recursos](feature-table.md).

## <a name="remarks"></a>Comentários

Para determinar se um produto foi definido para ser completamente desinstalado, um autor de pacote pode usar uma expressão condicional para verificar se REMOVE = ALL. Observe que, se o produto for removido definindo seu principal recurso como ausente, a propriedade **Remove** poderá não ser igual a All após a [ação InstallValidate](installvalidate-action.md). Isso significa que qualquer ação personalizada que dependa de REMOVE = ALL deve ser sequenciada após o InstallValidate. Para obter mais informações, consulte também [ações de condicionamento a serem executadas durante a remoção](conditioning-actions-to-run-during-removal.md). Observe que os nomes dos recursos diferenciam maiúsculas de minúsculas.

O instalador sempre avalia as seguintes propriedades na seguinte ordem:

1.  [**ADDLOCAL**](addlocal.md)
2.  **EXCLU**
3.  [**Addsource**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Install**](reinstall.md)
6.  [**ANUNCI**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por exemplo, se a linha de comando especificar ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source. Se a linha de comando for addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para executar-de-source.

O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




