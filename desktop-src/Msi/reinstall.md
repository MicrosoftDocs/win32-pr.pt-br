---
description: O valor da propriedade reinstalar é uma lista de recursos delimitados por vírgulas que devem ser reinstaladas. Os recursos listados devem estar presentes na coluna recurso da tabela de recursos. Para reinstalar todos os recursos, use REINSTALL = ALL na linha de comando.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: Reinstalar Propriedade
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749577"
---
# <a name="reinstall-property"></a>Reinstalar Propriedade

O valor da propriedade **reinstalar** é uma lista de recursos delimitados por vírgulas que devem ser reinstaladas. Os recursos listados devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md) . Para reinstalar todos os recursos, use REINSTALL = ALL na linha de comando.

## <a name="remarks"></a>Comentários

Observe que os nomes dos recursos diferenciam maiúsculas de minúsculas.

Se a propriedade **reinstalar** for definida, a propriedade [**REINSTALLMODE**](reinstallmode.md) também deverá ser definida para indicar o tipo de reinstalação a ser executada. Se a propriedade **REinstallmode** não estiver definida, por padrão, todos os arquivos que estão instalados no momento serão reinstalados, se o arquivo atualmente instalado for uma versão menor (ou não estiver presente). Por padrão, nenhuma entrada de registro é reescrita.

Observe que, mesmo se a **reinstalação** for definida como todos, somente os recursos que já foram instalados anteriormente serão reinstalados. Assim, se a **reinstalação** for definida para um produto que ainda está instalado, nenhuma ação de instalação ocorrerá.

O instalador sempre avalia as seguintes propriedades na seguinte ordem:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**EXCLU**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  **Install**
6.  [**ANUNCI**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**FILEADDLOCAL**](fileaddlocal.md)
10. [**FILEADDSOURCE**](fileaddsource.md)
11. [**FILEADDDEFAULT**](fileadddefault.md)

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

 

 




