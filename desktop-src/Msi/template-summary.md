---
description: Para um pacote de instalação, a propriedade de resumo do modelo indica as versões de plataforma e idioma que são compatíveis com esse banco de dados de instalação.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Propriedade de resumo do modelo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775698"
---
# <a name="template-summary-property"></a>Propriedade de resumo do modelo

Para um pacote de instalação, a propriedade de **Resumo do modelo** indica as versões de plataforma e idioma que são compatíveis com esse banco de dados de instalação. A sintaxe das informações de propriedade de **Resumo do modelo** para um banco de dados de instalação é a seguinte:

\[*propriedade de plataforma* \] ; \[ *ID do idioma* \] \[ ,*ID de idioma* \] \[ ,... \] .

Os exemplos a seguir são valores válidos para a propriedade de **Resumo do modelo** :

-   x64; 1033
-   Intel; 1033
-   Intel64; 1033
-   ; 1033
-   Intel; 1033, 2046
-   Intel64; 1033, 2046
-   Intel; 0
-   ARM; 1033, 2046
-   ARM; 0
-   Arm64; 1033, 2046
-   Arm64; 0

A propriedade **Summary do modelo** de uma transformação indica as versões de plataforma e idioma compatíveis com a transformação. Em um arquivo de transformação, apenas um idioma pode ser especificado. A plataforma e o idioma especificados determinam se uma transformação pode ser aplicada a um determinado banco de dados. A propriedade Platform e a propriedade Language poderão ser deixadas em branco se nenhuma restrição de transformação depender delas para validar a transformação.

A propriedade de **Resumo do modelo** de um pacote de patch é uma lista delimitada por ponto-e-vírgula dos códigos de produto que podem aceitar o patch. Se você usar [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) para gerar o pacote de patch, essa lista será obtida da [tabela TargetImages](targetimages-table-patchwiz-dll-.md) do arquivo de criação de patch.

Essa propriedade de resumo é necessária.

## <a name="remarks"></a>Comentários

Se a plataforma atual não corresponder a uma das plataformas especificadas na propriedade de **Resumo do modelo** , o instalador não processará o pacote.

Se a especificação da plataforma estiver ausente no valor da propriedade de **Resumo do modelo** , o instalador assumirá a arquitetura Intel.

Se esse for um pacote de Windows Installer de 64 bits sendo executado em uma plataforma Intel64 (Itanium), digite Intel64 na propriedade **Resumo do modelo** .

Se esse for um pacote de Windows Installer de 64 bits sendo executado em uma plataforma x64, digite x64 na propriedade de **Resumo do modelo** .

Se esse for um pacote de Windows Installer de 64 bits sendo executado em uma plataforma Arm64, digite Arm64 na propriedade **Resumo do modelo** .

Um pacote Windows Installer não pode ser marcado como compatível com Intel64 e x64; por exemplo, o valor da propriedade de **Resumo do modelo** de Intel64, x64 é inválido.

Um pacote Windows Installer não pode ser marcado como compatível com plataformas de 32 bits e 64 bits; por exemplo, os valores de propriedade de **Resumo do modelo** , como Intel, x64 ou Intel, Intel64 são inválidos.

Inserir 0 (zero) no campo ID de idioma da propriedade **Resumo do modelo** ou deixar esse campo vazio, indica que o pacote é neutro de idioma.

Se esse for um pacote Windows Installer sendo executado no Windows RT, insira o ARM de valor na propriedade de **Resumo do modelo** .

Os módulos de mesclagem são os únicos pacotes que podem ter vários idiomas. Somente um idioma pode ser especificado em um banco de dados do instalador de origem. Para obter mais informações, consulte [vários módulos de mesclagem de idiomas](multiple-language-merge-modules.md).

A plataforma Alpha não tem suporte pelo Windows Installer.

**Windows Installer:** Não há suporte para a sintaxe a seguir:

\[*Propriedade* \] \[ de plataforma,*propriedade de plataforma* \] \[ ,... \] \[ *ID do idioma* \] \[ ,*ID de idioma* \] \[ ,... \] .

Os exemplos a seguir não são valores válidos para a propriedade de **Resumo do modelo** :

-   Alpha, Intel; 1033
-   Intel, Alpha; 1033
-   Alfa; 1033
-   Alpha; 1033, 2046

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




