---
description: Fornece informações de status sobre um teste de hardware de um volume de sistema operacional totalmente descriptografado.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Método GetHardwareTestStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 32d0d477459dbc7352d1d8f6779c5c76cfbd537d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475352"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>Método GetHardwareTestStatus da classe Win32 \_ EncryptableVolume

O método **GetHardwareTestStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) fornece informações de status sobre um teste de hardware de um volume de sistema operacional totalmente descriptografado.

Use esse método para mostrar se um teste de hardware está pendente, bem como o êxito ou a falha de um teste de hardware concluído na última reinicialização do computador. Para solicitar um teste de hardware, use o método [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TestStatus* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Especifica se um teste de hardware está pendente, bem como o sucesso da falha de um teste de hardware concluído na última reinicialização do computador.




| Valor | Significado | 
|-------|---------|
| <span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl><dt><strong>NotFailed_and_NonePending</strong></dt><dt>0</dt></dl> | Se um teste foi solicitado, o teste foi bem-sucedido na última reinicialização do computador e a criptografia do volume agora está em andamento. Para obter o status de criptografia, consulte o método <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> . Caso contrário, nenhum teste foi executado na última reinicialização do computador e nenhum está pendente. <br /> | 
| <span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl><dt><strong>Com falha</strong></dt><dt>1</dt></dl> | A criptografia do volume não foi iniciada. Todos os protetores de chave foram removidos.<br /> Para resolver um teste com falha:<br /><ul><li>Consulte as informações no parâmetro <em>TestError</em> .</li><li>Adicione protetores de chave e use o método <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> novamente.</li></ul> | 
| <span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl><dt><strong>Pendente</strong></dt><dt>2</dt></dl> | Um teste foi solicitado e será executado na próxima reinicialização do computador.<br /> | 




 

</dd> <dt>

*TestError* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Especifica o erro do último teste de hardware concluído.



| Valor                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | Nenhum erro ocorreu ou nenhum teste de hardware foi executado na última reinicialização do computador.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003C)</dt> </dl> | FVE \_ E \_ keyfile \_ não \_ encontrado<br/> Uma unidade flash USB com um arquivo de chave externa não foi encontrada. Se essa falha persistir, o computador não poderá ler unidades USB durante a reinicialização. Talvez você não consiga usar chaves externas para desbloquear o volume do sistema operacional durante a reinicialização.<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003D)</dt> </dl> | FVE \_ E \_ keyfile \_ inválido<br/> O arquivo de chave externa na unidade flash USB estava corrompido. Tente uma unidade flash USB diferente para armazenar o arquivo de chave externa.<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003F)</dt> </dl> | FVE \_ E \_ TPM \_ desabilitado<br/> O TPM está desabilitado ou desativado ou desabilitado e desativado. Para ativar o TPM, use o provedor WMI do [**\_ TPM do Win32**](win32-tpm.md) ou execute o snap-in de gerenciamento do TPM (TPM. msc).<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041)</dt> </dl> | FVE \_ E \_ TPM \_ inválido \_ PCR<br/> O TPM detectou uma alteração nos serviços de reinicialização do sistema operacional no perfil de validação da plataforma atual. Remova qualquer CD ou DVD de inicialização do computador. Se essa falha persistir, verifique se as atualizações mais recentes do firmware e do BIOS estão instaladas e se o TPM está funcionando corretamente.<br/> |
| <dl> <dt>2150694979 (0x80310043)</dt> </dl>  | \_PIN FVE \_ E \_ inválido<br/> O PIN fornecido estava incorreto.<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

A tabela a seguir lista alguns dos códigos de retorno comuns.



| Código/valor de retorno                                                                                                                                                                  | Descrição                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | O volume está bloqueado.<br/> |



 

## <a name="remarks"></a>Comentários

Para solicitar um teste de hardware, use o método [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .

Para executar um teste de hardware quando seu status estiver pendente, siga estas etapas:

1.  Insira no computador uma unidade flash USB que contenha um arquivo de chave externa. Esta etapa se aplica somente se o volume tiver um protetor de chave do tipo "chave externa" ou "TPM e chave de inicialização".
2.  Reinicie o computador. Na reinicialização do computador, o teste de hardware é executado automaticamente.

Para cancelar o teste de hardware, use o método [**Encrypt**](encrypt-win32-encryptablevolume.md) .

Um teste bem-sucedido determina que:

-   O TPM poderá desbloquear o volume se houver um protetor de chave relacionado ao TPM.
-   O computador pode ler uma unidade flash USB que contém um arquivo de chave externa durante a inicialização se o volume puder ser desbloqueado por uma chave externa (incluindo uma chave de inicialização).

Os resultados de teste de hardware não estarão disponíveis após as alterações na conversão ou após a próxima reinicialização do computador. Verifique o log de eventos do sistema para obter as informações sobre os testes de hardware que foram executados anteriormente no computador.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Enterprise, \[ somente aplicativos de área de trabalho do vista Ultimate Windows\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
