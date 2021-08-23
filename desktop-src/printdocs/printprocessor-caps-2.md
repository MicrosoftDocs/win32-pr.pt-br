---
description: Representa informações de funcionalidade da impressora.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: PRINTPROCESSOR_CAPS_2 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3425f9477b153721980e3bb44b919b0baea37aa645caea6a3ee328a9ff923eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824726"
---
# <a name="printprocessor_caps_2-structure"></a>Estrutura PRINTPROCESSOR \_ CAPS \_ 2

Representa informações de funcionalidade da impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwLevel**
</dt> <dd>

Um valor que indica o número de versão da estrutura.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Uma máscara de bits que representa os vários números de páginas de documento que a impressora pode imprimir em um único lado de uma planilha física. O bit menos significativo representa uma página de documento por lado, o próximo bit representa duas páginas de documento por lado e assim por diante. Por exemplo, 0x0000810B indica que a impressora dá suporte a 1, 2, 4, 9 e 16 páginas de documento por lado físico.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Um valor de sinalizador que indica a ordem na qual as páginas serão impressas. Pode ser **NORMAL \_ PRINT,** **REVERSE \_ PRINT** ou **BOOKLET \_ PRINT.**

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

O número máximo de cópias que a impressora pode manipular.

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

Os padrões disponíveis quando várias páginas de documento são impressas no mesmo lado de uma folha de papel. Os sinalizadores possíveis são os seguintes:



| Valor                     | Significado                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| PPCAPS \_ À DIREITA \_ E, EM \_ SEGUIDA, PARA BAIXO | As páginas aparecem em linhas da direita para a esquerda, cada linha subsequente abaixo de seu antecessor.                 |
| PPCAPS \_ PARA BAIXO E PARA A \_ \_ DIREITA | As páginas aparecem em colunas de cima para baixo, cada coluna subsequente à direita de seu antecessor. |
| PPCAPS \_ À ESQUERDA \_ E, EM \_ SEGUIDA, PARA BAIXO  | As páginas aparecem em linhas da esquerda para a direita, cada linha subsequente abaixo de seu antecessor.                 |
| PPCAPS \_ PARA BAIXO E PARA A \_ \_ ESQUERDA  | As páginas aparecem em colunas de cima para baixo, cada coluna subsequente à esquerda de seu antecessor.  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

Pode ser apenas PPCAPS BORDER PRINT, indicando que, quando várias páginas de documento estão sendo impressas em um único lado de uma planilha física, a impressora pode ser informada se deve ou não imprimir uma borda em torno da área de imagem de cada página de \_ \_ documento.

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

Só pode ser PPCAPS \_ BOOKLET \_ EDGE, indicando que a impressora pode imprimir o estilo do livreto.

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| Valor                                         | Significado                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PÁGINAS INVERSAS PPCAPS \_ \_ PARA DUPLEX \_ \_ \_ REVERSO  | Ao imprimir em ordem inversa e duplexação, o processador pode imprimir a troca da ordem de cada par de páginas, portanto, em vez de imprimir na ordem 4,3,2,1, eles serão impressos na ordem 3,4,1,2.                                                                                                       |
| PPCAPS \_ NÃO ENVIA PÁGINAS EXTRAS PARA \_ \_ \_ \_ \_ DUPLEX | Ao duplexar, o Processador de Impressão pode ser informado para não enviar uma página extra quando houver um número ímpar de páginas de documento. O processador vai seguir o valor da melhor maneira possível, mas nos casos em que impedir uma página em branco extra causaria uma saída incorreta, as páginas extras ainda podem ser enviadas. |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

Só pode ser PPCAPS \_ SQUARE \_ SCALING, indicando que a impressora pode dimensionar a imagem da página.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores para todos os membros da estrutura são fornecidos pela **função GetPrintProcessorCapabilities,** que está documentada no Windows Driver Kit.

Quando um aplicativo chama [**GetPrinterData**](getprinterdata.md), o spooler chama a função **GetPrintProcessorCapabilities** de um processador de impressão e especifica um nome de valor que tem um formato de tipo de dados **PrintProcCaps, \_** em que *datatype* é o nome de um tipo de dados de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




