---
description: Representa informações de capacidade da impressora.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Estrutura de PRINTPROCESSOR_CAPS_2 (winspool. h)
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
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763245"
---
# <a name="printprocessor_caps_2-structure"></a>Estrutura do multiprocessador- \_ Caps \_ 2

Representa informações de capacidade da impressora.

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

Uma máscara de bits que representa os vários números de páginas de documentos que a impressora pode imprimir em um único lado de uma folha física. O bit menos significativo representa uma página de documento por lado, o próximo bit representa 2 páginas de documento por lado e assim por diante. Por exemplo, 0x0000810B indica que a impressora dá suporte a 1, 2, 4, 9 e 16 páginas de documento por lado físico.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Um valor de sinalizador que indica a ordem em que as páginas serão impressas. Pode ser impressão **normal \_**, **\_ impressão reversa** ou **\_ impressão de livretos**.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

O número máximo de cópias que a impressora pode manipular.

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

Os padrões disponíveis quando várias páginas de documento são impressas no mesmo lado de uma folha de papel. Os possíveis sinalizadores são os seguintes:



| Valor                     | Significado                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| PPCAPS \_ direita \_ e \_ abaixo | As páginas aparecem em linhas da direita para a esquerda, cada linha subsequente abaixo de sua predecessora.                 |
| PPCAPS \_ para baixo e para a \_ \_ direita | As páginas aparecem em colunas de cima para baixo, cada coluna subsequente à direita de seu predecessor. |
| PPCAPS \_ à esquerda \_ e \_ para baixo  | As páginas aparecem em linhas da esquerda para a direita, cada linha subsequente abaixo de sua predecessora.                 |
| PPCAPS \_ para baixo e para a \_ \_ esquerda  | As páginas aparecem em colunas de cima para baixo, cada coluna subsequente à esquerda de seu predecessor.  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

Pode ser apenas PPCAPS \_ \_ a impressão de borda, indicando que, quando várias páginas de documento estão sendo impressas em um único lado de uma folha física, a impressora pode ser informada se deseja ou não imprimir uma borda em torno da área de imagem de cada página do documento.

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

Só pode ser a \_ borda do livreto PPCAPS \_ , indicando que a impressora pode imprimir o estilo do livreto.

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| Valor                                         | Significado                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PPCAPS \_ páginas inversas \_ \_ para \_ duplex reverso \_  | Ao imprimir na ordem inversa e no duplex, o processador pode imprimir a ordem de cada par de páginas, portanto, em vez de imprimir na ordem 4, 3, 2, 1, eles serão impressos na ordem 3, 4, 1, 2.                                                                                                       |
| PPCAPS \_ não \_ Enviar \_ \_ páginas extras \_ para \_ duplex | Ao duplex, o processador de impressão pode ser instruído a não enviar uma página extra quando há um número ímpar de páginas de documento. O processador respeitará o valor da melhor maneira possível, mas nos casos em que a prevenção de uma página em branco extra poderia causar uma saída incorreta, as páginas extras ainda poderão ser enviadas. |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

Só pode ser PPCAPS \_ em \_ escala quadrada, indicando que a impressora pode dimensionar a imagem da página.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores para todos os membros da estrutura são fornecidos pela função **GetPrintProcessorCapabilities** , que está documentada no kit de driver do Windows.

Quando um aplicativo chama [**GetPrinterData**](getprinterdata.md), o spooler chama uma função **GetPrintProcessorCapabilities** do processador de impressão e especifica um nome de valor que tem um formato de _DataType_ **PrintProcCaps \_**, em que *DataType* é o nome de um tipo de dados de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




