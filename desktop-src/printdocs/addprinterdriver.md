---
description: A função AddPrinterDriver instala um driver de impressora local ou remoto e associa a configuração, os dados e os arquivos de driver.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Função AddPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662608"
---
# <a name="addprinterdriver-function"></a>Função AddPrinterDriver

A função **AddPrinterDriver** instala um driver de impressora local ou remoto e associa a configuração, os dados e os arquivos de driver.

Para obter mais flexibilidade na instalação ou atualização de drivers de impressora, use a função [**AddPrinterDriverEx**](addprinterdriverex.md) porque ela permite a atualização estrita, o downgrade estrito, a cópia somente de arquivos mais recentes e a cópia de todos os arquivos (independentemente dos carimbos de data/hora do arquivo).

> [!Note]  
> A instalação de um driver de impressora sem um pacote de driver não é mais recomendada. Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) em vez disso.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o driver deve ser instalado.

Se *pname* for **nulo**, o driver será instalado localmente.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A versão da estrutura à qual o *pDriverInfo* aponta.

Esse valor pode ser 2, 3, 4, 6 ou 8.

</dd> <dt>

*pDriverInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura que contém informações de driver de impressora. Isso depende do valor do *nível*.



| Valor | Estrutura da unidade da impressora                  |
|-------|------------------------------------------|
| 2     | [**Informações do DRIVER \_ \_ 2**](driver-info-2.md) |
| 3     | [**Informações do DRIVER \_ \_ 3**](driver-info-3.md) |
| 4     | [**Informações do DRIVER \_ \_ 4**](driver-info-4.md) |
| 6     | [**Informações do DRIVER \_ \_ 6**](driver-info-6.md) |
| 8     | [**Informações do DRIVER \_ \_ 8**](driver-info-8.md) |



 

Se o membro **pEnvironment** da estrutura apontada por *pDriverInfo* for **NULL**, o ambiente atual do chamador/cliente (não do destino/servidor) será usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Antes que um aplicativo chame a função **AddPrinterDriver** , todos os arquivos exigidos pelo driver devem ser copiados para o diretório de driver de impressora do sistema. Um aplicativo pode recuperar o nome desse diretório chamando a função [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .

Um aplicativo pode determinar quais drivers de impressora estão instalados no momento chamando a função [**EnumPrinterDrivers**](enumprinterdrivers.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddPrinterDriverW** (Unicode) e **AddPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 3**](driver-info-3.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 4**](driver-info-4.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

