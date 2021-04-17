---
description: O valor da propriedade FILEADDDEFAULT é uma lista de chaves de arquivo delimitadas por vírgulas que são instaladas em sua configuração padrão.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: Propriedade FILEADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789779"
---
# <a name="fileadddefault-property"></a>Propriedade FILEADDDEFAULT

O valor da propriedade **FILEADDDEFAULT** é uma lista de chaves de arquivo delimitadas por vírgulas que são instaladas em sua configuração padrão. Para cada chave de arquivo na lista, o instalador determina o componente que controla esse arquivo e instala o recurso que requer o menor espaço em disco. As chaves de arquivo na lista devem estar presentes na coluna arquivo da tabela de [arquivos](file-table.md) . Um recurso é instalado no mesmo estado de instalação como se o usuário tivesse solicitado uma instalação sob demanda do recurso. O estado é determinado pelo qual os bits são definidos para o recurso na coluna atributos da [tabela de recursos](feature-table.md)e quais bits são definidos para os componentes do recurso na coluna atributos da [tabela de componentes](component-table.md).

## <a name="remarks"></a>Comentários

Observe que os nomes de chave de arquivo diferenciam maiúsculas de minúsculas. Observe também que, se o sinalizador de bit SourceOnly for definido na coluna atributos da tabela de [componentes](component-table.md) de um componente, o componente será instalado para ser executado da origem.

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
11. [**FILEADDSOURCE**](fileaddsource.md)
12. **FILEADDDEFAULT**

Por exemplo, se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source. Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local e, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para execução-da-source.

O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




