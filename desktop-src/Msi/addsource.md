---
description: O valor da propriedade addsource é uma lista de recursos delimitados por vírgulas e que devem ser instalados para serem executados da origem.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: Propriedade addsource
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420ca53a96ddeb379a7e021db2c45157861acfb62d066cadfc7a163db7fbc307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078156"
---
# <a name="addsource-property"></a>Propriedade addsource

O valor da propriedade **addsource** é uma lista de recursos delimitados por vírgulas e que devem ser instalados para serem executados da origem. Os recursos devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md). Para instalar todos os recursos como executar da origem, use addsource = todos na linha de comando. Não insira addsource = todos na tabela de [Propriedades](property-table.md), pois isso gera um pacote de execução do código-fonte que não pode ser removido corretamente.

## <a name="remarks"></a>Comentários

Os nomes dos recursos diferenciam maiúsculas de minúsculas. Se o sinalizador de bit LocalOnly for definido na coluna atributos da [tabela de componentes](component-table.md) para um componente de um recurso na lista, esse componente será instalado para ser executado localmente.

O instalador sempre avalia as seguintes propriedades na seguinte ordem:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**EXCLU**](remove.md)
3.  **Addsource**
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Install**](reinstall.md)
6.  [**ANUNCI**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por exemplo:

-   Se a linha de comando especificar: ADDLOCAL = todos, addsource = **MyFeature**, todos os recursos serão definidos primeiro como Run-local e **MyFeature** será definido como Run-from-Source.
-   Se a linha de comando for: addsource = todos, ADDLOCAL =**MyFeature**, primeiro **MyFeature** estiver definido como Run-local e, quando addsource = All for avaliado, todos os recursos (incluindo **MyFeature**) serão redefinidos para execução-da-source.

O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




