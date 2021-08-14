---
description: A função AddPrinterDriverEx instala um driver de impressora local ou remota e vincula a configuração, os dados e os arquivos de driver.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Função AddPrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 00bd65ad415a97bbab825e4a13c8ad985d1d7f9b79d7b46e3f8f7ea6b5e5f0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868805"
---
# <a name="addprinterdriverex-function"></a>Função AddPrinterDriverEx

A função **AddPrinterDriverEx** instala um driver de impressora local ou remota e vincula a configuração, os dados e os arquivos de driver. Além de ter os recursos do [**AddPrinterDriver**](addprinterdriver.md), ele também tem opções que permitem a atualização estrita, o downgrade estrito, a cópia de arquivos mais recentes e a cópia de todos os arquivos (independentemente dos carimbos de data/hora do arquivo).

> [!Note]  
> A instalação de um driver de impressora sem um pacote de driver não é mais recomendada. Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) em vez disso.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o driver deve ser instalado. Se esse parâmetro for **nulo**, a função instalará o driver no computador local.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A versão da estrutura à qual o *pDriverInfo* aponta. Esse valor pode ser 2, 3, 4, 6 ou 8.

</dd> <dt>

*pDriverInfo* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura que contém informações de driver de impressora. Pode ser um dos seguintes.



| Valor do nível                                                                                       | \_Estrutura de informações do driver \_ \*                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**Informações do DRIVER \_ \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**Informações do DRIVER \_ \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**Informações do DRIVER \_ \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**Informações do DRIVER \_ \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**Informações do DRIVER \_ \_ 8**](driver-info-8.md)<br/> |



 

Se o membro **pEnvironment** da estrutura apontada por *pDriverInfo* for **NULL**, a função usará o ambiente atual do chamador/cliente, não o ambiente do destino/servidor.

</dd> <dt>

*dwFileCopyFlags* \[ no\]
</dt> <dd>

As opções para copiar os arquivos de driver. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**APD \_ copiar \_ todos os \_ arquivos**</dt> </dl>                | Adicione o driver de impressora e copie todos os arquivos no diretório de driver de impressora. Os carimbos de data/hora do arquivo são ignorados com essa opção.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**APD \_ copiar \_ do \_ diretório**</dt> </dl> | Adicione o driver de impressora usando os nomes de arquivo totalmente qualificados especificados na estrutura [**informações do driver \_ \_ 6**](driver-info-6.md) . Esse sinalizador é vinculada em conjunto com um dos outros sinalizadores de cópia. Se esse sinalizador for definido, **AddPrinterDriverEx** falhará se os arquivos não existirem onde eles estiverem especificados na estrutura informações do **Driver \_ \_ 6** . Os arquivos não precisam ser copiados para o diretório do driver de impressora do sistema. Consulte os comentários.<br/> **Windows 2000:** Não há suporte para esse sinalizador.<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**APD \_ copiar \_ novos \_ arquivos**</dt> </dl>                | Adicione o driver de impressora e copie os arquivos no diretório de driver de impressora que são mais novos do que os arquivos correspondentes que estão em uso no momento. Esse sinalizador emula o comportamento de [**AddPrinterDriver**](addprinterdriver.md).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**\_downgrade estrito \_ APD**</dt> </dl>           | Adicione o driver de impressora somente se todos os arquivos no diretório de driver de impressora forem mais antigos do que quaisquer arquivos correspondentes em uso no momento.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**APD \_ de \_ atualização estrita**</dt> </dl>                 | Adicione o driver de impressora somente se todos os arquivos no diretório de driver de impressora forem mais novos do que os arquivos correspondentes em uso no momento.<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

Se o driver de impressora tiver problemas para funcionar com o sistema operacional, o **AddPrinterDriverEx** falhará com um dos seguintes códigos de erro:



| Código do Erro                      | Significado                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Driver de impressora de erro \_ \_ \_ bloqueado | O driver não funciona no sistema operacional.                                                                                                         |
| ERRO \_ de \_ Driver de impressora \_ avisado  | O driver não é confiável no sistema operacional. No entanto, se APD \_ instalar \_ \_ o driver avisado for especificado, o driver será instalado e nenhum aviso será fornecido. |



 

Para obter mais informações, consulte Comentários.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Antes de chamar a função **AddPrinterDriverEx** , todos os arquivos exigidos pelo driver devem ser copiados para o diretório de driver de impressora do sistema. Para recuperar o nome desse diretório, chame a função [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .

Para determinar quais drivers de impressora estão instalados no momento, chame a função [**EnumPrinterDrivers**](enumprinterdrivers.md) .

Se o driver de impressora tiver sido adicionado com êxito, a função chamará a função DrvDriverEvent (inicialização de evento de DRIVER \_ \_ , nível, \_ informações \_ \* de driver, lParam) para permitir que o driver execute as inicializações necessárias durante a instalação de um driver de impressora. para obter mais informações sobre o **DrvDriverEvent**, consulte o Microsoft Windows Driver Development Kit (DDK)

O driver não deve usar uma chamada de interface do usuário durante a chamada para **DrvDriverEvent**. Para fazer trabalhos relacionados à interface do usuário, o instalador deve usar a entrada VendorSetup no arquivo. inf da impressora ou, para dispositivos Plug and Play, o instalador pode usar um coinstalador específico do dispositivo. Para obter mais informações sobre VendorSetup, consulte o DDK.

Os arquivos que são referenciados na [**estrutura \_ informações \_ sobre o driver 6**](driver-info-6.md) devem ser locais no computador do qual a chamada é feita. Um nome de arquivo pode ser um nome UNC, desde que o nome UNC seja o computador local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddPrinterDriverExW** (Unicode) e **AddPrinterDriverExA** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 3**](driver-info-3.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 4**](driver-info-4.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 6**](driver-info-6.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

