---
description: Inicia a criptografia de um volume totalmente descriptografado ou retoma a criptografia de um volume parcialmente criptografado.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Método Encrypt da classe Win32_EncryptableVolume dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e6e2ed0eea4bb9c70949a3916733bf2777397fcb509ba0ce2f91633bf15a74d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892464"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Método Encrypt da classe EncryptableVolume do Win32 \_

O **método Encrypt** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) inicia a criptografia de um volume totalmente descriptografado ou retoma a criptografia de um volume parcialmente criptografado. Quando a criptografia está em pausa ou em andamento, esse método se comporta da mesma forma que [**ResumeConversion.**](resumeconversion-win32-encryptablevolume.md) Quando a descriptografia é pausada ou em andamento, esse método interrompe a descriptografia e inicia a criptografia.

> [!Note]  
> Se a unidade for criptografada por hardware, esse método não criptografa dados. Em vez disso, ele define o status da banda como "desbloqueado" de "sempre desbloqueado". Se a faixa estiver bloqueada, desbloqueada ou for somente leitura, a unidade será considerada criptografada.

 

**Windows Vista:** Não há suporte para a criptografia de um volume diferente do volume do sistema operacional em execução no momento.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncryptionMethod* \[ in, opcional\]
</dt> <dd>

Tipo: **uint32**

Um inteiro sem sinal que especifica o algoritmo de criptografia e o tamanho da chave usados para criptografar o volume. Se esse parâmetro for maior que zero e o volume for parcial ou totalmente criptografado, *EncryptionMethod* deverá corresponder ao método de criptografia existente do volume. Se esse parâmetro for maior que zero e a configuração de Política de Grupo correspondente estiver habilitada com um valor válido, *EncryptionMethod* deverá corresponder à configuração Política de Grupo configuração.

Para obter uma lista de possíveis valores encryptionMethod, consulte [**o método GetEncryptionMethod.**](getencryptionmethod-win32-encryptablevolume.md)

O valor padrão Windows 7 ou abaixo é: 1 (AES \_ 128 \_ WITH \_ DIFFUSER).

O valor padrão para Windows 8, Windows 8.1 ou Windows 10 versão 1507 é: 3 (AES \_ 128).

O valor padrão para Windows 10, versão 1511 ou superior é: 6 (XTS \_ AES \_ 128).

</dd> <dt>

*EncryptionFlags* \[ in, opcional\]
</dt> <dd>

Tipo: **uint32**

Sinalizadores que descrevem o comportamento de criptografia.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise e Windows Server 2008:** Esse parâmetro não está disponível.

Uma combinação de 32 bits com os bits a seguir definidos no momento.



| Valor                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Execute a criptografia de volume no modo de criptografia somente de dados ao iniciar o novo processo de criptografia. Se a criptografia tiver sido pausada ou interrompida, chamar o **método Encrypt** retomará efetivamente a conversão e o valor desse bit será ignorado. Esse bit só tem efeito quando os métodos **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) iniciam a criptografia do estado totalmente descriptografado, descriptografia em estado de andamento ou estado em pausa de descriptografia. Se esse bit for zero, o que significa que ele não está definido, ao iniciar o novo processo de criptografia, a conversão de modo completo será executada.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Execute o apagando sob demanda do espaço livre do volume. Chamar o **método Encrypt** com esse conjunto de bits só é permitido quando o volume não está convertendo ou apagando no momento e está em um estado "criptografado".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Execute a operação solicitada de forma síncrona. A chamada será interrompida até que a operação solicitada seja concluída ou tenha sido interrompida. Esse sinalizador só tem suporte com o **método Encrypt.** Esse sinalizador pode ser especificado quando **Encrypt** é chamado para retomar a criptografia interrompida ou interrompida ou apagamento ou quando a criptografia ou a limpeza está em andamento. Isso permite que o chamador retome a espera síncrona até que o processo seja concluído ou interrompido.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Esse método retorna imediatamente. Se o volume já estiver totalmente criptografado e nenhum outro erro for retornado, esse método retornará 0.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor/código de retorno</th>
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
<td>O <em>parâmetro EncryptionMethod</em> é fornecido, mas não está dentro do intervalo conhecido ou não faz a Política de Grupo atual.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>Não existe nenhuma chave de criptografia para o volume. Desabilite os protetores de chave usando o <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>método DisableKeyProtectors</strong></a> ou use um dos seguintes métodos para especificar protetores de chave para o volume:<br/>
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<strong>Windows Vista:</strong> Quando não houver nenhuma chave de criptografia para o volume, ERROR_INVALID_OPERATION será retornado. O valor decimal é 4317 e o valor hexadecimal é 0x10DD.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </dl></td>
<td>O método de criptografia fornecido não é igual ao do volume parcial ou totalmente criptografado. Para continuar a criptografia, deixe o parâmetro <em>EncryptionMethod</em> em branco ou use um valor de zero.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>O volume não pode ser criptografado porque este computador está configurado para fazer parte de um cluster de servidores.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </dl></td>
<td>O volume está bloqueado.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>Nenhum protetor de chave do tipo &quot; Senha Numérica &quot; é especificado. O Política de Grupo requer um backup de informações de recuperação para Active Directory Domain Services. Para adicionar pelo menos um protetor de chave desse tipo, use o <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>método ProtectKeyWithNumericalPassword.</strong></a><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Quando você usa esse método sem o segundo parâmetro opcional (de acordo com a definição do Windows 7 e Windows Vista Enterprise), o método sempre iniciará a conversão de modo completo para manter o comportamento compatível com versões anteriores. Dessa forma, a expectativa de segurança de aplicativos e scripts existentes não será interrompida com a adição do segundo parâmetro opcional no Windows 8 e Windows Server 2012.

Você pode chamar [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) para determinar se a criptografia está em andamento e o percentual do volume que foi criptografado.

Depois que o volume for totalmente criptografado e se os protetores de chave foram adicionados e habilitados, o status de proteção do volume muda para "ativado".

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows aplicativos da área de trabalho do Vista Ultimate \[\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
