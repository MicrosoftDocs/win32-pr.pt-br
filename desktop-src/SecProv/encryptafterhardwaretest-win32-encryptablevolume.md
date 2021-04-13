---
description: Inicia a criptografia de um volume de sistema operacional totalmente descriptografado após um teste de hardware.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Método EncryptAfterHardwareTest da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501534"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a>Método EncryptAfterHardwareTest da classe Win32 \_ EncryptableVolume

O método **EncryptAfterHardwareTest** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) começa a criptografia de um volume de sistema operacional totalmente descriptografado após um teste de hardware. Uma reinicialização é necessária para executar este teste de hardware. Use esse método em vez do método [**Encrypt**](encrypt-win32-encryptablevolume.md) para verificar se o BitLocker funcionará conforme o esperado.

> [!Note]  
> Se o disco rígido estiver criptografado para hardware, esse método não criptografará os dados. Em vez disso, ele define o status da banda como desbloqueado de "permanente desbloqueado". Se a banda estiver bloqueada, desbloqueada ou for somente leitura, a unidade será considerada criptografada.

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncryptionMethod* \[ em, opcional\]
</dt> <dd>

Tipo: **UInt32**

Especifica o algoritmo de criptografia e o tamanho da chave usados para criptografar o volume. Deixe esse parâmetro em branco para usar o valor padrão de zero. Se o volume for parcialmente ou totalmente criptografado, o valor desse parâmetro deverá ser 0 ou corresponder ao método de criptografia existente do volume. Se a configuração de Política de Grupo correspondente tiver sido habilitada com um valor válido, o valor desse parâmetro deverá ser 0 ou corresponder à configuração de Política de Grupo.

Se a configuração de Política de Grupo correspondente for inválida, o padrão de AES 128 com difusor será usado.



| Valor                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**Não especificado**</dt> <dt>0</dt> </dl> | Use a configuração de Política de Grupo atual, se disponível e válida, caso contrário, o método de criptografia padrão.<br/>                                                                              |
| <dl> <dt>1</dt> </dl>                                                                                                                                                                | AES 128 COM DIFUSOR<br/> Criptografe o volume usando o algoritmo de criptografia AES (AES) aprimorado com uma camada de difusor e usando um tamanho de chave AES de 128 bits.<br/> |
| <dl> <dt>2</dt> </dl>                                                                                                                                                                | AES 256 COM DIFUSOR<br/> Criptografe o volume usando o algoritmo de criptografia AES (AES) aprimorado com uma camada de difusor e usando um tamanho de chave AES de 256 bits.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                          | Criptografe o volume usando o algoritmo criptografia AES (AES) e usando um tamanho de chave AES de 128 bits.<br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                          | Criptografe o volume usando o algoritmo criptografia AES (AES) e usando um tamanho de chave AES de 256 bits.<br/>                                                                 |



 

</dd> <dt>

*EncryptionFlags* \[ em, opcional\]
</dt> <dd>

Tipo: **UInt32**

Sinalizadores que descrevem o comportamento de criptografia.

**Windows 7, Windows server 2008 R2, Windows Vista Enterprise e Windows server 2008:** Este parâmetro não está disponível.

Uma combinação de 32 bits com os seguintes bits definidos no momento.



| Valor                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Execute a criptografia de volume no modo de criptografia somente de dados ao iniciar o novo processo de criptografia. Se a criptografia tiver sido pausada ou interrompida, chamar o método [**Encrypt**](encrypt-win32-encryptablevolume.md) efetivamente retomará a conversão e o valor desse bit será ignorado. Esse bit só tem efeito quando os métodos **Encrypt** ou **EncryptAfterHardwareTest** iniciam a criptografia do estado totalmente descriptografado, a descriptografia em estado de andamento ou o status de descriptografia em pausa. Se esse bit for zero, o que significa que ele não está definido, ao iniciar o novo processo de criptografia, a conversão de modo completo será executada.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Execute o apagamento sob demanda do espaço livre no volume. A chamada do método [**Encrypt**](encrypt-win32-encryptablevolume.md) com esse conjunto de bits só é permitida quando o volume não está convertendo ou apagando e está em um estado "criptografado".<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>0x00010000 </dt> </dl> | Execute a operação solicitada de forma síncrona. A chamada será bloqueada até que a operação solicitada seja concluída ou interrompida. Só há suporte para esse sinalizador com o método [**Encrypt**](encrypt-win32-encryptablevolume.md) . Esse sinalizador pode ser **especificado quando a criptografia é** chamada para retomar a criptografia interrompida ou interrompida ou apagar ou quando a criptografia ou o apagamento estiver em andamento. Isso permite que o chamador retome de forma síncrona aguardando até que o processo seja concluído ou interrompido.<br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Esse método retorna imediatamente. Se o volume já estiver totalmente criptografado e nenhum outro erro for retornado, esse método retornará zero.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código/valor de retorno</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </dl></td>
<td>O método foi bem-sucedido.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </dl></td>
<td>O parâmetro <em>EncryptionMethod</em> é fornecido, mas não está dentro do intervalo conhecido ou não corresponde à configuração de política de grupo atual.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>Não existe chave de criptografia para o volume.<br/> Desabilite protetores de chave usando o método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou use um dos seguintes métodos para especificar protetores de chave para o volume:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>O volume não pode ser criptografado porque este computador está configurado para fazer parte de um cluster de servidores.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </dl></td>
<td>Nenhum protetor de chave do tipo &quot; TPM &quot; , &quot; TPM e PIN &quot; , &quot; TPM e PIN e chave de inicialização &quot; , &quot; TPM e chave de inicialização &quot; ou &quot; chave externa &quot; podem ser encontrados. O teste de hardware só envolve os protetores de chave anteriores.<br/> Se você ainda quiser executar um teste de hardware, deverá usar um dos seguintes métodos para especificar protetores de chave para o volume:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </dl></td>
<td>O volume é parcialmente ou totalmente criptografado.<br/> O teste de hardware se aplica antes que ocorra a criptografia. Se você ainda quiser executar o teste, primeiro use o método <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> e, em seguida, use um dos seguintes métodos para adicionar protetores de chave:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </dl></td>
<td>O volume é um volume de dados.<br/> O teste de hardware aplica-se somente a volumes que podem iniciar o sistema operacional. Execute este método no volume do sistema operacional atualmente iniciado.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>Nenhum protetor de chave da &quot; senha numérica de tipo &quot; foi especificado. O Política de Grupo requer um backup das informações de recuperação para Active Directory Domain Services. Para adicionar pelo menos um protetor de chave desse tipo, use o método <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Quando você usa esse método sem o segundo parâmetro opcional (de acordo com a definição do Windows 7 e do Windows Vista Enterprise), o método sempre iniciará a conversão em modo completo para manter o comportamento compatível com versões anteriores. Dessa forma, a expectativa de segurança de aplicativos e scripts existentes não será quebrada com a adição do segundo parâmetro opcional no Windows 8 e no Windows Server 2012.

Ao contrário do método [**Encrypt**](encrypt-win32-encryptablevolume.md) , esse método faz o seguinte:

-   Testa se o TPM poderá desbloquear o volume, se existir um protetor de chave relacionado ao TPM.
-   Testa se o computador pode ler uma unidade flash USB que contém um arquivo de chave externa durante o início, se o volume for desbloqueado por uma chave externa (incluindo uma chave de inicialização).
-   Requer uma reinicialização do computador para executar o teste de hardware.
-   Inicia a criptografia somente se o teste de hardware tiver sucesso.
-   Não pode ser usado em um volume de dados, em um volume parcialmente ou totalmente criptografado ou para retomar a criptografia.

Antes de executar esse método, use os seguintes métodos para criar os protetores de chave relacionados:

-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Depois de executar esse método, execute estas etapas adicionais:

1.  Insira no computador uma unidade flash USB que contenha um arquivo de chave externa. Esta etapa se aplica somente se o volume tiver um protetor de chave do tipo "chave externa" ou "TPM e chave de inicialização".
2.  Reinicie o computador.

Na reinicialização do computador, o teste de hardware é executado automaticamente.

A criptografia começa se o teste de hardware for executado com sucesso. Caso contrário, tente resolver quaisquer falhas de hardware. Execute [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) depois de reiniciar o computador para obter os resultados do teste.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]<br/>                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
