---
description: As informações da impressora \_ \_ 6 especificam o valor de status de uma impressora.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Estrutura de PRINTER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771362"
---
# <a name="printer_info_6-structure"></a>Estrutura de informações da impressora \_ \_ 6

As **informações da impressora \_ \_ 6** especificam o valor de status de uma impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwStatus**
</dt> <dd>

O status da impressora. Esse membro pode ser qualquer combinação razoável dos valores a seguir.



| Valor                               | Significado                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| STATUS da impressora \_ \_ ocupado               | A impressora está ocupada.                                                                                          |
| porta de status da impressora \_ \_ \_ aberta         | A porta da impressora está aberta.                                                                                     |
| \_erro de status da impressora \_              | Não usado.                                                                                                     |
| \_inicialização do status da impressora \_       | A impressora está sendo inicializada.                                                                                  |
| STATUS da impressora \_ \_ e/s \_ ativa         | A impressora está em um estado de entrada/saída ativo                                                                |
| \_ \_ feed manual de status da impressora \_       | A impressora está em um estado de feed manual.                                                                        |
| STATUS da impressora \_ \_ sem \_ toner          | A impressora está sem toner.                                                                                  |
| STATUS da impressora \_ \_ não \_ disponível     | A impressora não está disponível para impressão.                                                                    |
| STATUS da impressora \_ \_ offline            | A impressora está offline.                                                                                       |
| \_status \_ da impressora fora \_ da \_ memória    | A impressora ficou sem memória.                                                                            |
| bandeja de saída de status da impressora \_ \_ \_ \_ cheia  | O compartimento de saída da impressora está cheio.                                                                             |
| \_ \_ apontador de página de status da impressora \_         | A impressora não pode imprimir a página atual.                                                                    |
| \_ \_ emperramento de papel do status da impressora \_         | O papel está emperrado na impressora                                                                                |
| \_saída do status da impressora \_ \_         | A impressora está sem papel.                                                                                  |
| \_problema de \_ papel do status da impressora \_     | A impressora tem um problema de papel.                                                                              |
| STATUS da impressora em \_ \_ pausa             | A impressora está em pausa.                                                                                        |
| \_exclusão de status \_ da impressora pendente \_  | A exclusão da impressora está pendente como resultado de uma chamada para a função [**DeletePrinter**](deleteprinter.md) . |
| \_economia de \_ energia de status da impressora \_        | A impressora está no modo de economia de energia.                                                                            |
| \_impressão de status da impressora \_           | A impressora está imprimindo.                                                                                      |
| \_processamento de status da impressora \_         | A impressora está processando um comando da função [**Setprinter**](setprinter.md) .                       |
| servidor de status de impressora \_ \_ \_ desconhecido    | O status da impressora é desconhecido.                                                                                |
| \_toner de status da impressora \_ \_ baixo         | A impressora está com pouco toner.                                                                                  |
| \_status da \_ impressora \_ intervenção do usuário | A impressora tem um erro que exige que o usuário faça algo.                                              |
| STATUS da impressora \_ \_ aguardando            | A impressora está aguardando.                                                                                       |
| STATUS da impressora \_ \_ aquecendo \_        | A impressora está em preparação.                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações de impressora \_ \_ 6W** (Unicode) e **\_ info de impressora \_ \_ 6a** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Informações da impressora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**Informações da impressora \_ \_ 5**](printer-info-5.md)
</dt> </dl>

 

 




