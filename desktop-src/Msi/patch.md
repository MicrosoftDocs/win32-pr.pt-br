---
description: O instalador define a propriedade PATCH para uma lista de patches que estão sendo aplicados chamando MsiApplyPatch, MsiApplyMultiplePatches ou a opção de linha de comando/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: Propriedade PATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747746"
---
# <a name="patch-property"></a>Propriedade PATCH

O instalador define a propriedade **patch** para uma lista de patches que estão sendo aplicados chamando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) ou a opção de [linha de comando](command-line-options.md)/p. Você também pode definir a propriedade **patch** na linha de comando ao instalar um pacote usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou a opção de linha de comando/i.

O valor da propriedade **patch** é uma lista dos patches que estão sendo instalados. Cada patch na lista é representado pelo caminho completo para o pacote do patch (arquivo. msp). Os caminhos completos na lista são separados por ponto e vírgula.

**Windows Installer 2,0:** Não há suporte para vários patches. Windows Installer 3,0 é necessário para aplicar vários patches.

## <a name="remarks"></a>Comentários

Se você criar um pacote de patch usando [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) você poderá especificar que uma ação ou uma caixa de diálogo seja executada somente quando um patch específico estiver sendo aplicado. Ao criar o pacote de patch, por exemplo test. msp, você cria uma imagem atualizada do produto e um arquivo de propriedades de criação de patch. Ao criar o arquivo de propriedades de criação de patch, você pode inserir um nome de propriedade, por exemplo, PATCHFORTEST, no campo MediaSrcPropName da tabela [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) . Ao criar as tabelas de sequência da imagem atualizada do produto, você pode incluir na coluna condição da tabela de sequência uma instrução condicional para a ação ou caixa de diálogo que você deseja tornar condicional.

Por exemplo, você pode usar a seguinte instrução condicional para executar uma ação ou caixa de diálogo somente quando Test. msp estiver sendo aplicado.

<dl> PATCH E PATCHFORTEST E PATCH >< PATCHFORTEST  
</dl>

> [!Note]  
> Como a propriedade **patch** pode conter vários patches, use o operador de subcadeia de caracteres "><" para testar a presença de um patch específico em vez do operador Equals "=". Para obter mais informações sobre instruções condicionais, consulte a seção [sintaxe de instrução condicional](conditional-statement-syntax.md) .

 

O instalador definirá as duas propriedades se você aplicar uma lista de patches que inclui o Test. msp. Por exemplo, você pode usar a [opção de linha de comando](command-line-options.md) /p para aplicar uma lista de dois patches.

**msiexec/QB/p \\ \\ temporário \\ \\ \\ patches XYZ \\ Tests. msp; \\ \\ rascunho do rascunho da \\ \\ \\ barra XYZ. msp**

O instalador define as propriedades **patch** e PATCHFORTEST da seguinte maneira.

<dl> PATCH = \\ \\ rascunho \\ temporário \\ \\ patches de XYZ \\ Test. msp; \\ \\ rascunho do rascunho da \\ \\ \\ barra XYZ. msp  
PATCHFORTEST = rascunho \\ \\ \\ temporário \\ \\ patches do XYZ \\ Test. msp  
</dl>

Nesse caso, a condição é verdadeira e a caixa de diálogo ou ação condicional acima pode ser executada para cada patch que está sendo instalado, Test. msp e bar. msp.

Se Test. msp não estiver sendo aplicado, o instalador não o incluirá na propriedade **patch** e não definirá PATCHFORTEST. Nesse caso, a condição acima é falsa e a ação condicional ou a caixa de diálogo não é executada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sintaxe de instrução condicional](conditional-statement-syntax.md)
</dt> <dt>

[Exemplos de sintaxe de instrução condicional](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




