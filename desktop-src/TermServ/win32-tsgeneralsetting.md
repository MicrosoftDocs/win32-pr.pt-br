---
title: Classe Win32_TSGeneralSetting
description: Representa as configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGeneralSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGeneralSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644718"
---
# <a name="win32_tsgeneralsetting-class"></a><span data-ttu-id="4d668-105">\_Classe Win32 TSGeneralSetting</span><span class="sxs-lookup"><span data-stu-id="4d668-105">Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="4d668-106">A classe WMI **\_ TSGeneralSetting do Win32** representa as configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="4d668-106">The **Win32\_TSGeneralSetting** WMI class represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

<span data-ttu-id="4d668-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="4d668-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="4d668-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="4d668-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d668-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d668-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="4d668-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4d668-110">Members</span></span>

<span data-ttu-id="4d668-111">A classe **Win32 \_ TSGeneralSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4d668-111">The **Win32\_TSGeneralSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="4d668-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d668-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4d668-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4d668-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4d668-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d668-114">Methods</span></span>

<span data-ttu-id="4d668-115">A classe **Win32 \_ TSGeneralSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4d668-115">The **Win32\_TSGeneralSetting** class has these methods.</span></span>



| <span data-ttu-id="4d668-116">Método</span><span class="sxs-lookup"><span data-stu-id="4d668-116">Method</span></span>                                                                                        | <span data-ttu-id="4d668-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d668-117">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d668-118">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="4d668-118">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)                       | <span data-ttu-id="4d668-119">Define o nível de criptografia.</span><span class="sxs-lookup"><span data-stu-id="4d668-119">Sets the encryption level.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="4d668-120">**SetSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="4d668-120">**SetSecurityLayer**</span></span>](win32-tsgeneralsetting-setsecuritylayer.md)                           | <span data-ttu-id="4d668-121">Define a camada de segurança como uma "camada de segurança RDP" (0), "Negotiate" (1) ou "SSL" (2).</span><span class="sxs-lookup"><span data-stu-id="4d668-121">Sets the security layer to one of "RDP Security Layer" (0), "Negotiate" (1), or "SSL" (2).</span></span><br/>                                                                   |
| [<span data-ttu-id="4d668-122">**SetUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="4d668-122">**SetUserAuthenticationRequired**</span></span>](setuserauthenticationrequired-win32-tsgeneralsetting.md) | <span data-ttu-id="4d668-123">Habilita ou desabilita o requisito de que os usuários devem ser autenticados no momento da conexão, definindo o valor da propriedade **UserAuthenticationRequired** .</span><span class="sxs-lookup"><span data-stu-id="4d668-123">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4d668-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4d668-124">Properties</span></span>

<span data-ttu-id="4d668-125">A classe **Win32 \_ TSGeneralSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4d668-125">The **Win32\_TSGeneralSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d668-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="4d668-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d668-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4d668-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4d668-130">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="4d668-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="4d668-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d668-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d668-132">**CertificateName**</span><span class="sxs-lookup"><span data-stu-id="4d668-132">**CertificateName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-135">Nome de exibição do nome da entidade do certificado pessoal do computador local.</span><span class="sxs-lookup"><span data-stu-id="4d668-135">Display name for the local computer personal certificate subject name.</span></span>

</dd> <dt>

<span data-ttu-id="4d668-136">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="4d668-136">**Certificates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-137">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="4d668-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4d668-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-139">Contém um repositório de certificados serializado que contém todos os certificados do repositório de **contas do meu usuário** no computador que são certificados de servidor válidos para uso com SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="4d668-139">Contains a serialized certificate store that contains all of the certificates from the **My user account** store on the computer that are valid server certificates for use with secure sockets layer (SSL).</span></span>

</dd> <dt>

<span data-ttu-id="4d668-140">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="4d668-140">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4d668-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d668-143">Nome descritivo da combinação de camada de sessão e protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="4d668-143">Descriptive name of the combination of session layer and transport protocol.</span></span>

</dd> <dt>

<span data-ttu-id="4d668-144">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4d668-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-147">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="4d668-147">Description of the object.</span></span>

<span data-ttu-id="4d668-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d668-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d668-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4d668-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-150">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4d668-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d668-152">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="4d668-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="4d668-153">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="4d668-153">The date the object was installed.</span></span> <span data-ttu-id="4d668-154">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="4d668-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4d668-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d668-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d668-156">**MinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="4d668-156">**MinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d668-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d668-159">Qualificadores: **baixo** ("somente os dados enviados do cliente para o servidor são protegidos pela criptografia com base na intensidade de chave padrão do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d668-159">Qualifiers: **Low** ("Only data sent from client to server is protected by encryption based on server's standard key strength.</span></span> <span data-ttu-id="4d668-160">Os dados enviados do servidor para o cliente não estão protegidos. "), **médio** (" todos os dados enviados entre o servidor e o cliente são protegidos pela criptografia com base na intensidade de chave padrão do servidor. "), **alta** (" todos os dados enviados entre o servidor e o cliente são protegidos pela criptografia de chave máxima baseada no servidor. ")</span><span class="sxs-lookup"><span data-stu-id="4d668-160">Data sent from Server to client is not protected."), **Medium** ("All data sent between Server and client is protected by encryption based on server's standard key strength."), **High** ("All data sent between Server and client is protected by encryption based onserver's maximum key strength.")</span></span>
</dt> </dl>

<span data-ttu-id="4d668-161">O nível mínimo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="4d668-161">The minimum encryption level.</span></span>

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="4d668-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (1)</span><span class="sxs-lookup"><span data-stu-id="4d668-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-163">Nível baixo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="4d668-163">Low level of encryption.</span></span> <span data-ttu-id="4d668-164">Somente os dados enviados do cliente para o servidor são criptografados usando a criptografia de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="4d668-164">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="4d668-165">Lembre-se de que os dados enviados do servidor para o cliente não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="4d668-165">Be aware that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span data-ttu-id="4d668-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Compatível com médio/cliente** (2)</span><span class="sxs-lookup"><span data-stu-id="4d668-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medium / Client Compatible** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-167">Nível de criptografia compatível com o cliente.</span><span class="sxs-lookup"><span data-stu-id="4d668-167">Client compatible level of encryption.</span></span> <span data-ttu-id="4d668-168">Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados na força de chave máxima com suporte do cliente.</span><span class="sxs-lookup"><span data-stu-id="4d668-168">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="4d668-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (3)</span><span class="sxs-lookup"><span data-stu-id="4d668-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-170">Alto nível de criptografia.</span><span class="sxs-lookup"><span data-stu-id="4d668-170">High level of encryption.</span></span> <span data-ttu-id="4d668-171">Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados usando criptografia de 128 bits de alta segurança.</span><span class="sxs-lookup"><span data-stu-id="4d668-171">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="4d668-172">Os clientes que não dão suporte a esse nível de criptografia não podem se conectar.</span><span class="sxs-lookup"><span data-stu-id="4d668-172">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span data-ttu-id="4d668-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Compatível com FIPS** (4)</span><span class="sxs-lookup"><span data-stu-id="4d668-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS Compliant** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-174">Criptografia compatível com FIPS.</span><span class="sxs-lookup"><span data-stu-id="4d668-174">FIPS compliant encryption.</span></span> <span data-ttu-id="4d668-175">Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados e descriptografados com os algoritmos de criptografia do padrão FIPS (FIPS) usando os módulos criptográficos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d668-175">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="4d668-176">O FIPS é um padrão intitulado "requisitos de segurança para módulos criptográficos".</span><span class="sxs-lookup"><span data-stu-id="4d668-176">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="4d668-177">O FIPS 140-1 (1994) e o FIPS 140-2 (2001) descrevem os requisitos governamentais dos módulos de criptografia de hardware e software usados no governo dos EUA.</span><span class="sxs-lookup"><span data-stu-id="4d668-177">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d668-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4d668-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-181">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="4d668-181">The name of the object.</span></span>

<span data-ttu-id="4d668-182">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d668-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d668-183">**PolicySourceMinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="4d668-183">**PolicySourceMinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-184">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d668-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-186">Indica se a propriedade **MinEncryptionLevel** está configurada pelo servidor, por política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="4d668-186">Indicates whether the **MinEncryptionLevel** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="4d668-187">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="4d668-187">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-188">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d668-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d668-189">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d668-189">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-190">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="4d668-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="4d668-191">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4d668-191">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-192">Padrão</span><span class="sxs-lookup"><span data-stu-id="4d668-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d668-193">**PolicySourceSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="4d668-193">**PolicySourceSecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-194">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d668-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-196">Indica se a propriedade **SecurityLayer** está configurada pelo servidor, por política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="4d668-196">Indicates whether the **SecurityLayer** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="4d668-197">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="4d668-197">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-198">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d668-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d668-199">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d668-199">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-200">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="4d668-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="4d668-201">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4d668-201">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-202">Padrão</span><span class="sxs-lookup"><span data-stu-id="4d668-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d668-203">**PolicySourceUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="4d668-203">**PolicySourceUserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-204">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d668-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-206">Indica se a propriedade **UserAuthenticationRequired** está configurada pelo servidor, por política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="4d668-206">Indicates whether the **UserAuthenticationRequired** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="4d668-207">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="4d668-207">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-208">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d668-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d668-209">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d668-209">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-210">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="4d668-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="4d668-211">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4d668-211">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-212">Padrão</span><span class="sxs-lookup"><span data-stu-id="4d668-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d668-213">**SecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="4d668-213">**SecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-214">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d668-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d668-216">Qualificadores: **RDPSecurityLayer** ("camada de segurança de RDP: comunicação entre o serverand o cliente usará a criptografia RDP nativa."), **Negotiate** ("a camada mais segura com suporte do cliente será usada. Se houver suporte, o TLS 1,0 será usado. "), o **SSL** (" SSL (TLS 1,0) será usado para autenticação de servidor, bem como forencrypting todos os dados transferidos entre o servidor e o cliente. Essa configuração exige que o servidor tenha um certificado compatível com SSL. "), **NEWTBD** (" uma nova camada de segurança no Longhorn. ")</span><span class="sxs-lookup"><span data-stu-id="4d668-216">Qualifiers: **RDPSecurityLayer** ("RDP Security Layer: Communication between the serverand the client will use native RDP encryption."), **Negotiate** ("The most secure layer that is supported by the client will be used.If supported, TLS 1.0 will be used."), **SSL** ("SSL (TLS 1.0) will be used for server authentication as well as forencrypting all data transferred between the server and the client.This setting requires the server to have an SSL compatible certificate."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN.")</span></span>
</dt> </dl>

<span data-ttu-id="4d668-217">Especifica a camada de segurança usada entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="4d668-217">Specifies the security layer used between the client and server.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="4d668-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Camada de segurança RDP** (1)</span><span class="sxs-lookup"><span data-stu-id="4d668-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-219">A comunicação entre o servidor e o cliente usa a criptografia RDP nativa.</span><span class="sxs-lookup"><span data-stu-id="4d668-219">Communication between the server and the client uses native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="4d668-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negociar** (2)</span><span class="sxs-lookup"><span data-stu-id="4d668-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-221">A camada mais segura com suporte do cliente é usada.</span><span class="sxs-lookup"><span data-stu-id="4d668-221">The most secure layer that is supported by the client is used.</span></span> <span data-ttu-id="4d668-222">Se houver suporte, o SSL (TLS 1,0) será usado.</span><span class="sxs-lookup"><span data-stu-id="4d668-222">If supported, SSL (TLS 1.0) is used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="4d668-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span><span class="sxs-lookup"><span data-stu-id="4d668-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-224">SSL (TLS 1,0) é usado para autenticação de servidor e para criptografar todos os dados transferidos entre o servidor e o cliente.</span><span class="sxs-lookup"><span data-stu-id="4d668-224">SSL (TLS 1.0) is used for server authentication and for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="4d668-225">Essa configuração requer que o servidor tenha um certificado compatível com SSL.</span><span class="sxs-lookup"><span data-stu-id="4d668-225">This setting requires the server to have an SSL-compatible certificate.</span></span> <span data-ttu-id="4d668-226">Essa configuração não é compatível com um valor de **MinEncryptionLevel** de 1.</span><span class="sxs-lookup"><span data-stu-id="4d668-226">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span data-ttu-id="4d668-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span><span class="sxs-lookup"><span data-stu-id="4d668-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-228">Uma nova camada de segurança.</span><span class="sxs-lookup"><span data-stu-id="4d668-228">A new security layer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d668-229">**SSLCertificateSHA1Hash**</span><span class="sxs-lookup"><span data-stu-id="4d668-229">**SSLCertificateSHA1Hash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-231">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4d668-231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d668-232">Especifica o hash SHA1 no formato hexadecimal do certificado SSL para o servidor de destino a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4d668-232">Specifies the SHA1 hash in hexadecimal format of the SSL certificate for the target server to use.</span></span>

<span data-ttu-id="4d668-233">A impressão digital de um certificado pode ser encontrada usando o snap-in de certificados do MMC na guia detalhes da página Propriedades do certificado.</span><span class="sxs-lookup"><span data-stu-id="4d668-233">The thumbprint of a certificate may be found using the Certificates MMC snap-in on the Details tab of the certificate properties page.</span></span>

</dd> <dt>

<span data-ttu-id="4d668-234">**SSLCertificateSHA1HashType**</span><span class="sxs-lookup"><span data-stu-id="4d668-234">**SSLCertificateSHA1HashType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-235">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d668-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-237">Indica o estado da propriedade **SSLCertificateSHA1Hash** .</span><span class="sxs-lookup"><span data-stu-id="4d668-237">Indicates the state of the **SSLCertificateSHA1Hash** property.</span></span>

<dt>

<span data-ttu-id="4d668-238">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="4d668-238">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-239">Inválido</span><span class="sxs-lookup"><span data-stu-id="4d668-239">Not valid</span></span>

</dd> <dt>

<span data-ttu-id="4d668-240">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d668-240">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-241">Padrão autoassinado</span><span class="sxs-lookup"><span data-stu-id="4d668-241">Default self-signed</span></span>

</dd> <dt>

<span data-ttu-id="4d668-242">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4d668-242">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-243">Política de grupo padrão imposta</span><span class="sxs-lookup"><span data-stu-id="4d668-243">Default group policy enforced</span></span>

</dd> <dt>

<span data-ttu-id="4d668-244">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="4d668-244">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="4d668-245">Personalizado</span><span class="sxs-lookup"><span data-stu-id="4d668-245">Custom</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d668-246">**Status**</span><span class="sxs-lookup"><span data-stu-id="4d668-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d668-249">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="4d668-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="4d668-250">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="4d668-250">Current status of the object.</span></span> <span data-ttu-id="4d668-251">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="4d668-251">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4d668-252">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="4d668-252">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4d668-253">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="4d668-253">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4d668-254">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="4d668-254">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4d668-255">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="4d668-255">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4d668-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d668-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="4d668-257">("OK")</span><span class="sxs-lookup"><span data-stu-id="4d668-257">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d668-258">("Erro")</span><span class="sxs-lookup"><span data-stu-id="4d668-258">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d668-259">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="4d668-259">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d668-260">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="4d668-260">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d668-261">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4d668-261">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d668-262">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="4d668-262">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d668-263">("Parando")</span><span class="sxs-lookup"><span data-stu-id="4d668-263">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d668-264">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="4d668-264">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d668-265">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="4d668-265">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-266">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-268">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="4d668-268">The name of the terminal.</span></span>

<span data-ttu-id="4d668-269">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="4d668-269">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d668-270">**TerminalProtocol**</span><span class="sxs-lookup"><span data-stu-id="4d668-270">**TerminalProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-271">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-273">O nome do protocolo de camada de sessão; por exemplo, Microsoft RDP 5,0.</span><span class="sxs-lookup"><span data-stu-id="4d668-273">The name of the session layer protocol; for example, Microsoft RDP 5.0.</span></span>

</dd> <dt>

<span data-ttu-id="4d668-274">**Transport**</span><span class="sxs-lookup"><span data-stu-id="4d668-274">**Transport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-275">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4d668-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-277">O tipo de transporte usado na conexão; por exemplo, TCP, NetBIOS ou IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="4d668-277">The type of transport used in the connection; for example, TCP, NetBIOS, or IPX/SPX.</span></span>

</dd> <dt>

<span data-ttu-id="4d668-278">**UserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="4d668-278">**UserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-279">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d668-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4d668-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d668-281">Especifica o tipo de autenticação de usuário usado para conexões remotas.</span><span class="sxs-lookup"><span data-stu-id="4d668-281">Specifies the type of user authentication used for remote connections.</span></span> <span data-ttu-id="4d668-282">Se definido como 1, o que significa habilitado, o **UserAuthenticationRequired** exigirá a autenticação do usuário no momento da conexão para aumentar a proteção do servidor contra ataques à rede.</span><span class="sxs-lookup"><span data-stu-id="4d668-282">If set to 1, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="4d668-283">Somente clientes [protocolo RDP](remote-desktop-protocol.md) (RDP) que oferecem suporte a rdp versão 6,0 ou superior são capazes de se conectar.</span><span class="sxs-lookup"><span data-stu-id="4d668-283">Only [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="4d668-284">Para evitar interrupções para usuários remotos, é recomendável implantar clientes RDP que dão suporte à versão de protocolo apropriada antes de habilitar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="4d668-284">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

<span data-ttu-id="4d668-285">Use o método [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) para habilitar ou desabilitar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="4d668-285">Use the [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) method to enable or disable this property.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4d668-286"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="4d668-286"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-287">A autenticação do usuário na conexão está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d668-287">User authentication at connection is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4d668-288"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d668-288"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-289">A autenticação de usuário na conexão está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4d668-289">User authentication at connection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d668-290">**WindowsAuthentication**</span><span class="sxs-lookup"><span data-stu-id="4d668-290">**WindowsAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d668-291">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d668-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d668-292">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4d668-292">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d668-293">Especifica se a conexão usa como padrão o processo de autenticação padrão do Windows ou para outro pacote de autenticação que foi instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="4d668-293">Specifies whether the connection defaults to the standard Windows authentication process or to another authentication package that has been installed on the system.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4d668-294"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="4d668-294"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-295">O não usa como padrão o processo de autenticação padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="4d668-295">Does not default to the standard Windows authentication process.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4d668-296"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d668-296"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d668-297">O padrão é o processo de autenticação padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="4d668-297">Defaults to the standard Windows authentication process.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d668-298">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d668-298">Remarks</span></span>

<span data-ttu-id="4d668-299">Lembre-se de que as estações de janela não associadas à sessão de console não podem acessar os métodos e as propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="4d668-299">Be aware that window stations not associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="4d668-300">Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade Terminalname, os métodos desse objeto retornarão o **WBEM \_ E não \_ terão \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="4d668-300">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="4d668-301">Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto com a finalidade de adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="4d668-301">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="4d668-302">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="4d668-302">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="4d668-303">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="4d668-303">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="4d668-304">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="4d668-304">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="4d668-305">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="4d668-305">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="4d668-306">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4d668-306">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4d668-307">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4d668-307">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4d668-308">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="4d668-308">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4d668-309">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4d668-309">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d668-310">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d668-310">Requirements</span></span>



| <span data-ttu-id="4d668-311">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d668-311">Requirement</span></span> | <span data-ttu-id="4d668-312">Valor</span><span class="sxs-lookup"><span data-stu-id="4d668-312">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d668-313">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d668-313">Minimum supported client</span></span><br/> | <span data-ttu-id="4d668-314">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d668-314">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d668-315">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d668-315">Minimum supported server</span></span><br/> | <span data-ttu-id="4d668-316">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d668-316">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d668-317">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d668-317">Namespace</span></span><br/>                | <span data-ttu-id="4d668-318">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="4d668-318">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4d668-319">MOF</span><span class="sxs-lookup"><span data-stu-id="4d668-319">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d668-320"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d668-320"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d668-321">DLL</span><span class="sxs-lookup"><span data-stu-id="4d668-321">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d668-322"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d668-322"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d668-323">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d668-323">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d668-324">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="4d668-324">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

